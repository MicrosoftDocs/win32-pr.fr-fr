---
description: La \_ classe NFS CIM représente un système de fichiers distant monté, à l’aide du protocole NFS (Network File System), à partir d’un système informatique.
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: Classe CIM_NFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748588"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="3ed40-103">\_Classe NFS CIM</span><span class="sxs-lookup"><span data-stu-id="3ed40-103">CIM\_NFS class</span></span>

<span data-ttu-id="3ed40-104">La **classe \_ NFS CIM** représente un système de fichiers distant monté, à l’aide du protocole NFS (Network File System), à partir d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3ed40-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="3ed40-105">Les propriétés de l’objet NFS correspondent aux aspects opérationnels du montage et représentent la configuration côté client pour l’accès NFS.</span><span class="sxs-lookup"><span data-stu-id="3ed40-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="3ed40-106">Le type de système de fichiers doit être défini pour indiquer le type de système de fichiers tel qu’il apparaît au client.</span><span class="sxs-lookup"><span data-stu-id="3ed40-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ed40-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3ed40-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3ed40-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3ed40-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3ed40-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3ed40-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3ed40-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3ed40-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed40-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ed40-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
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
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="3ed40-112">Membres</span><span class="sxs-lookup"><span data-stu-id="3ed40-112">Members</span></span>

<span data-ttu-id="3ed40-113">La **classe \_ NFS CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3ed40-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="3ed40-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3ed40-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ed40-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3ed40-115">Properties</span></span>

<span data-ttu-id="3ed40-116">La **classe \_ NFS CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3ed40-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ed40-117">**AttributeCaching**</span><span class="sxs-lookup"><span data-stu-id="3ed40-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-118">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-120">Si la **valeur est true**, la mise en cache des attributs de contrôle est activée.</span><span class="sxs-lookup"><span data-stu-id="3ed40-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="3ed40-121">Si la **valeur est false**, le cache des attributs de contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3ed40-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-122">**AttributeCachingForDirectoriesMax**</span><span class="sxs-lookup"><span data-stu-id="3ed40-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-123">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-125">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-126">Nombre maximal de secondes pendant lesquelles les attributs mis en cache sont conservés après la mise à jour de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3ed40-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-127">**AttributeCachingForDirectoriesMin**</span><span class="sxs-lookup"><span data-stu-id="3ed40-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-128">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-130">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-131">Nombre minimal de secondes pendant lesquelles les attributs mis en cache sont conservés après la mise à jour de l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="3ed40-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-132">**AttributeCachingForRegularFilesMax**</span><span class="sxs-lookup"><span data-stu-id="3ed40-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-135">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-136">Nombre maximal de secondes pendant lesquelles les attributs mis en cache sont conservés après la modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="3ed40-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-137">**AttributeCachingForRegularFilesMin**</span><span class="sxs-lookup"><span data-stu-id="3ed40-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-140">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« secondes »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-141">Nombre minimal de secondes pendant lesquelles les attributs mis en cache sont conservés après la modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="3ed40-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-142">**AvailableSpace**</span><span class="sxs-lookup"><span data-stu-id="3ed40-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-143">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ed40-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-145">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,4 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" octets ")</span><span class="sxs-lookup"><span data-stu-id="3ed40-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-146">Quantité totale d’espace libre, en octets, pour le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3ed40-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="3ed40-147">S’il est inconnu, entrez 0.</span><span class="sxs-lookup"><span data-stu-id="3ed40-147">If unknown, enter 0.</span></span>

<span data-ttu-id="3ed40-148">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="3ed40-149">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ed40-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="3ed40-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-151">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ed40-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-153">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ed40-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-154">Les systèmes de fichiers peuvent lire ou écrire des données dans des blocs qui sont définis indépendamment des extensions de stockage sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="3ed40-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="3ed40-155">Cette propriété capture la taille de bloc du système de fichiers pour le stockage et la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="3ed40-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="3ed40-156">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="3ed40-157">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ed40-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ed40-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-161">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-162">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ed40-162">Short textual description of the object.</span></span>

<span data-ttu-id="3ed40-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-164">**CasePreserved**</span><span class="sxs-lookup"><span data-stu-id="3ed40-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-165">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-167">Si la **valeur est true**, la casse des noms de fichiers est conservée.</span><span class="sxs-lookup"><span data-stu-id="3ed40-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="3ed40-168">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="3ed40-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-172">Si la **valeur est true**, les noms de fichiers qui respectent la casse sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3ed40-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="3ed40-173">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-174">**Codes**</span><span class="sxs-lookup"><span data-stu-id="3ed40-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-177">Jeux de caractères ou encodage pris en charge par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3ed40-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="3ed40-178">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ed40-179">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3ed40-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3ed40-180">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3ed40-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="3ed40-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="3ed40-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="3ed40-182">**Unicode** (3)</span><span class="sxs-lookup"><span data-stu-id="3ed40-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="3ed40-183">**Iso2022** (4)</span><span class="sxs-lookup"><span data-stu-id="3ed40-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="3ed40-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="3ed40-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="3ed40-185">**Code UNIX étendu** (6)</span><span class="sxs-lookup"><span data-stu-id="3ed40-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="3ed40-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="3ed40-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="3ed40-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="3ed40-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ed40-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3ed40-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-191">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,7»)</span><span class="sxs-lookup"><span data-stu-id="3ed40-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-192">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3ed40-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3ed40-193">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3ed40-194">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3ed40-195">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="3ed40-196">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ed40-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-200">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3ed40-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-201">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="3ed40-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3ed40-202">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="3ed40-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3ed40-203">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-204">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ed40-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-207">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="3ed40-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-208">Portée du nom de la classe de création du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3ed40-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="3ed40-209">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="3ed40-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-213">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="3ed40-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-214">Nom du système d’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="3ed40-214">Scoping computer system's name.</span></span>

<span data-ttu-id="3ed40-215">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-216">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ed40-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-219">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3ed40-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-220">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ed40-220">Textual description of the object.</span></span>

<span data-ttu-id="3ed40-221">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="3ed40-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-225">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partition DMTF \| 002,8»)</span><span class="sxs-lookup"><span data-stu-id="3ed40-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-226">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3ed40-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="3ed40-227">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="3ed40-228">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="3ed40-229">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="3ed40-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="3ed40-230">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-231">**FileSystemSize**</span><span class="sxs-lookup"><span data-stu-id="3ed40-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-232">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ed40-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-234">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ed40-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-235">Taille totale du système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="3ed40-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="3ed40-236">S’il est inconnu, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="3ed40-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="3ed40-237">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="3ed40-238">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ed40-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-239">**ForegroundMount**</span><span class="sxs-lookup"><span data-stu-id="3ed40-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-240">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-242">Si la **valeur est true**, les nouvelles tentatives sont effectuées au premier plan.</span><span class="sxs-lookup"><span data-stu-id="3ed40-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="3ed40-243">Si la **valeur est false** et que la première tentative de montage échoue, les nouvelles tentatives sont effectuées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3ed40-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-244">**HardMount**</span><span class="sxs-lookup"><span data-stu-id="3ed40-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-247">Si la **valeur est true**, une fois le système de fichiers monté, les demandes NFS sont retentées jusqu’à ce que le système d’hébergement réponde.</span><span class="sxs-lookup"><span data-stu-id="3ed40-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="3ed40-248">Si la **valeur est false**, une erreur est retournée si le système d’hébergement ne répond pas après le montage du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3ed40-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ed40-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-250">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ed40-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-252">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="3ed40-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-253">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ed40-253">Date and time the object was installed.</span></span> <span data-ttu-id="3ed40-254">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="3ed40-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3ed40-255">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-256">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="3ed40-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-257">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-259">Si la **valeur est true**, les interruptions sont autorisées pour les montages matériels.</span><span class="sxs-lookup"><span data-stu-id="3ed40-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="3ed40-260">Si la **valeur est false**, les interruptions sont ignorées pour les montages matériels.</span><span class="sxs-lookup"><span data-stu-id="3ed40-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-261">**MaxFileNameLength**</span><span class="sxs-lookup"><span data-stu-id="3ed40-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ed40-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-264">Longueur maximale d’un nom de fichier dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3ed40-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="3ed40-265">La valeur 0 (zéro) indique qu’il n’existe aucune limite pour la longueur du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="3ed40-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="3ed40-266">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-267">**MountFailureRetries**</span><span class="sxs-lookup"><span data-stu-id="3ed40-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-268">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-270">Nombre maximal de nouvelles tentatives d’échec de montage autorisées.</span><span class="sxs-lookup"><span data-stu-id="3ed40-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-271">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3ed40-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-274">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3ed40-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-275">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="3ed40-275">Label by which the object is known.</span></span> <span data-ttu-id="3ed40-276">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="3ed40-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3ed40-277">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-278">**ReadBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3ed40-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-279">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ed40-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-281">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ed40-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-282">Taille de la mémoire tampon de lecture, en octets.</span><span class="sxs-lookup"><span data-stu-id="3ed40-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="3ed40-283">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ed40-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-284">**Lecture seule**</span><span class="sxs-lookup"><span data-stu-id="3ed40-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-285">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3ed40-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-287">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSAccess ")</span><span class="sxs-lookup"><span data-stu-id="3ed40-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-288">Si la **valeur est true**, le système de fichiers est désigné comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3ed40-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="3ed40-289">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-290">**RetransmissionAttempts**</span><span class="sxs-lookup"><span data-stu-id="3ed40-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-291">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ed40-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-293">Nombre maximal de retransmissions NFS autorisées.</span><span class="sxs-lookup"><span data-stu-id="3ed40-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-294">**RetransmissionTimeout**</span><span class="sxs-lookup"><span data-stu-id="3ed40-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-295">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ed40-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-297">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« dixièmes de secondes »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-298">Délai d’expiration NFS, en dixièmes de seconde.</span><span class="sxs-lookup"><span data-stu-id="3ed40-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-299">**Causes**</span><span class="sxs-lookup"><span data-stu-id="3ed40-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-302">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrFSMountPoint ")</span><span class="sxs-lookup"><span data-stu-id="3ed40-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-303">Nom de chemin d’accès ou d’autres informations qui définissent la racine du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3ed40-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="3ed40-304">Cette propriété est héritée [**du \_ système de fichiers CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-305">**ServerCommunicationPort**</span><span class="sxs-lookup"><span data-stu-id="3ed40-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-306">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ed40-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-308">Numéro de port UDP du système de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="3ed40-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="3ed40-309">**État**</span><span class="sxs-lookup"><span data-stu-id="3ed40-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3ed40-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-312">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3ed40-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-313">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ed40-313">Current status of the object.</span></span>

<span data-ttu-id="3ed40-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3ed40-315">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ed40-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3ed40-316">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3ed40-317">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3ed40-318">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ed40-319">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="3ed40-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3ed40-320">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3ed40-321">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3ed40-322">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3ed40-323">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3ed40-324">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3ed40-325">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3ed40-326">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3ed40-327">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="3ed40-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ed40-328">**WriteBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3ed40-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed40-329">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ed40-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3ed40-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed40-331">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ed40-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ed40-332">Taille de la mémoire tampon d’écriture, en octets.</span><span class="sxs-lookup"><span data-stu-id="3ed40-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="3ed40-333">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3ed40-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ed40-334">Notes</span><span class="sxs-lookup"><span data-stu-id="3ed40-334">Remarks</span></span>

<span data-ttu-id="3ed40-335">La **classe \_ NFS CIM** est dérivée de la [**\_ RemoteFileSystem CIM**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="3ed40-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="3ed40-336">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="3ed40-336">WMI does not implement this class.</span></span>

<span data-ttu-id="3ed40-337">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3ed40-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3ed40-338">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3ed40-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed40-339">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ed40-339">Requirements</span></span>



| <span data-ttu-id="3ed40-340">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ed40-340">Requirement</span></span> | <span data-ttu-id="3ed40-341">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ed40-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed40-342">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ed40-342">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed40-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ed40-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ed40-344">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ed40-344">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed40-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ed40-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ed40-346">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3ed40-346">Namespace</span></span><br/>                | <span data-ttu-id="3ed40-347">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3ed40-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ed40-348">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed40-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed40-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed40-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ed40-350">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed40-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed40-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed40-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed40-352">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ed40-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed40-353">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3ed40-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

