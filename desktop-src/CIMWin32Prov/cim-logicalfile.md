---
description: La \_ classe CIM LogicalFile représente une collection nommée de données, qui peut être du code exécutable, qui se trouve dans un système de fichiers sur une extension de stockage.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: Classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514921"
---
# <a name="cim_logicalfile-class"></a><span data-ttu-id="a6f2f-103">\_Classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="a6f2f-103">CIM\_LogicalFile class</span></span>

<span data-ttu-id="a6f2f-104">La classe **CIM \_ LogicalFile** représente une collection nommée de données, qui peut être du code exécutable, qui se trouve dans un système de fichiers sur une extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-104">The **CIM\_LogicalFile** class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6f2f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a6f2f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a6f2f-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a6f2f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f2f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6f2f-109">Syntax</span></span>

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="a6f2f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a6f2f-110">Members</span></span>

<span data-ttu-id="a6f2f-111">La classe **CIM \_ LogicalFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6f2f-111">The **CIM\_LogicalFile** class has these types of members:</span></span>

-   [<span data-ttu-id="a6f2f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a6f2f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6f2f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6f2f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6f2f-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a6f2f-114">Methods</span></span>

<span data-ttu-id="a6f2f-115">La classe **CIM \_ LogicalFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-115">The **CIM\_LogicalFile** class has these methods.</span></span>



| <span data-ttu-id="a6f2f-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a6f2f-116">Method</span></span>                                                                                             | <span data-ttu-id="a6f2f-117">Description</span><span class="sxs-lookup"><span data-stu-id="a6f2f-117">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6f2f-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | <span data-ttu-id="a6f2f-119">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="a6f2f-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="a6f2f-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | <span data-ttu-id="a6f2f-122">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="a6f2f-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="a6f2f-124">**Dens**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-124">**Compress**</span></span>](compress-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="a6f2f-125">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="a6f2f-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-127">**CompressEx**</span></span>](compressex-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="a6f2f-128">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-129">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="a6f2f-130">**Copier**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-130">**Copy**</span></span>](copy-method-in-class-cim-logicalfile.md)                                               | <span data-ttu-id="a6f2f-131">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="a6f2f-132">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="a6f2f-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-133">**CopyEx**</span></span>](copyex-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="a6f2f-134">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="a6f2f-135">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="a6f2f-136">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-136">**Delete**</span></span>](delete-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="a6f2f-137">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-138">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="a6f2f-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-logicalfile.md)                                       | <span data-ttu-id="a6f2f-140">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-141">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="a6f2f-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)           | <span data-ttu-id="a6f2f-143">Détermine si l’appelant dispose des autorisations agrégées spécifiées par l’argument d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="a6f2f-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="a6f2f-144">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="a6f2f-145">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-145">**Rename**</span></span>](rename-method-in-class-cim-logicalfile.md)                                           | <span data-ttu-id="a6f2f-146">Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-147">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="a6f2f-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-logicalfile.md)                             | <span data-ttu-id="a6f2f-149">Obtient la propriété du fichier logique (ou répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-149">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-150">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-150">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="a6f2f-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)                         | <span data-ttu-id="a6f2f-152">Obtient la propriété du fichier logique (ou répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-152">Obtains ownership of the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-153">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-153">Not implemented by WMI.</span></span><br/>                                    |
| [<span data-ttu-id="a6f2f-154">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-logicalfile.md)                                   | <span data-ttu-id="a6f2f-155">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-156">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="a6f2f-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-logicalfile.md)                               | <span data-ttu-id="a6f2f-158">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="a6f2f-159">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="a6f2f-160">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6f2f-160">Properties</span></span>

<span data-ttu-id="a6f2f-161">La classe **CIM \_ LogicalFile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-161">The **CIM\_LogicalFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6f2f-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-165">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-166">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-166">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="a6f2f-167">Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-167">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="a6f2f-168">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a6f2f-169">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-169">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="a6f2f-170">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-170">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="a6f2f-171">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-171">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="a6f2f-172">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-172">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="a6f2f-173">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-173">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="a6f2f-174">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-174">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="a6f2f-175">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-175">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="a6f2f-176">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-176">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="a6f2f-177">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-177">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="a6f2f-178">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-178">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="a6f2f-179">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-179">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="a6f2f-180">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-180">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="a6f2f-181">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-181">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="a6f2f-182">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-182">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6f2f-183">**Archive**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-183">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-186">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-187">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-187">If **True**, the file should be archived.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-188">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-191">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-192">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-192">A short textual description of the object.</span></span>

<span data-ttu-id="a6f2f-193">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-194">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-194">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-195">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-197">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-197">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-198">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-198">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-202">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-202">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-203">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-203">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="a6f2f-204">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-204">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="a6f2f-205">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-205">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="a6f2f-206">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-206">If the logical file is not compressed, use "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-210">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-210">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-211">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-211">Name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-212">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-212">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-213">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-215">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-215">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-216">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-216">Date and time of the file's creation.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-217">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-217">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-220">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-220">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-221">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-221">Class of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-222">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-222">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-225">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-225">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-226">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-226">Name of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-227">**Description**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-230">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-231">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-231">A textual description of the object.</span></span>

<span data-ttu-id="a6f2f-232">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-232">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-233">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-233">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-236">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-236">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-237">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-237">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="a6f2f-238">Cette propriété est héritée de la **\_ LogicalFile CIM**. Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="a6f2f-238">This property is inherited from **CIM\_LogicalFile**.Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-239">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-239">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-242">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-243">Nom de fichier compatible DOS.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-243">DOS-compatible file name.</span></span> <span data-ttu-id="a6f2f-244">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="a6f2f-244">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-245">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-245">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-246">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-246">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-248">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-248">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-249">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-249">If **True**, the file is encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-250">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-250">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-253">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-254">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-254">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="a6f2f-255">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-255">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="a6f2f-256">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-256">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="a6f2f-257">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-257">If the logical file is not encrypted, use "Not Encrypted".</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-258">**Extension**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-258">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-259">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-261">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-261">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-262">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-262">File name extension without the preceding period (dot).</span></span> <span data-ttu-id="a6f2f-263">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="a6f2f-263">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-264">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-264">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-265">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-267">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-267">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-268">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-268">File name without the file name extension.</span></span> <span data-ttu-id="a6f2f-269">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="a6f2f-269">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-271">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-273">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-274">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="a6f2f-275">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-276">**FileType**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-276">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-279">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-280">Descripteur qui représente le type de fichier indiqué par la propriété d' **extension** .</span><span class="sxs-lookup"><span data-stu-id="a6f2f-280">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-284">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-284">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-285">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-285">Class of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-286">**FSName**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-286">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-289">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-290">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-290">Name of the file system.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-291">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-291">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-292">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-294">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-295">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-295">If **True**, the file is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-296">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-296">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-297">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-297">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-299">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-300">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-300">Indicates when the object was installed.</span></span> <span data-ttu-id="a6f2f-301">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-301">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a6f2f-302">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-302">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-303">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-303">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-304">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-306">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-307">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-307">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="a6f2f-308">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-309">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-309">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-310">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-312">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-313">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-313">Date and time the file was last accessed.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-314">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-314">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-315">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-315">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-317">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-318">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-318">Date and time the file was last modified.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-319">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-322">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-322">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-323">La propriété Name est une chaîne représentant le nom hérité qui sert de clé à une instance de fichier logique dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-323">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="a6f2f-324">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-324">Full path names should be provided.</span></span> <span data-ttu-id="a6f2f-325">Exemple : C : \\ \\ système Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="a6f2f-325">Example: C:\\Windows\\system\\win.ini</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-326">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-326">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-327">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-329">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-329">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-330">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-330">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="a6f2f-331">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="a6f2f-331">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-332">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-332">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-333">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-335">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-336">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-336">If **True**, the file can be read.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-337">**État**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-340">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-340">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-341">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-341">String that indicates the current status of the object.</span></span> <span data-ttu-id="a6f2f-342">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-342">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a6f2f-343">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-343">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a6f2f-344">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-344">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a6f2f-345">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="a6f2f-345">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a6f2f-346">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-346">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a6f2f-347">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-347">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a6f2f-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a6f2f-349">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6f2f-349">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a6f2f-350">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-350">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a6f2f-351">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-351">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a6f2f-352">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-352">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6f2f-353">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="a6f2f-353">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a6f2f-354">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-354">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a6f2f-355">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-355">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a6f2f-356">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-356">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a6f2f-357">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-357">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a6f2f-358">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-358">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a6f2f-359">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-359">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a6f2f-360">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-360">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a6f2f-361">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-361">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6f2f-362">**Système**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-362">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-363">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-365">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-366">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-366">If **True**, the file is a system file.</span></span>

</dd> <dt>

<span data-ttu-id="a6f2f-367">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-367">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6f2f-368">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a6f2f-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6f2f-370">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="a6f2f-370">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="a6f2f-371">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-371">If **True**, the file can be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6f2f-372">Notes</span><span class="sxs-lookup"><span data-stu-id="a6f2f-372">Remarks</span></span>

<span data-ttu-id="a6f2f-373">La classe **CIM \_ LogicalFile** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-373">The **CIM\_LogicalFile** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a6f2f-374">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-374">WMI does not implement this class.</span></span> <span data-ttu-id="a6f2f-375">Pour les classes dérivées de **CIM \_ LogicalFile**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6f2f-375">For classes derived from **CIM\_LogicalFile**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a6f2f-376">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-376">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a6f2f-377">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a6f2f-377">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f2f-378">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6f2f-378">Requirements</span></span>



| <span data-ttu-id="a6f2f-379">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6f2f-379">Requirement</span></span> | <span data-ttu-id="a6f2f-380">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6f2f-380">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f2f-381">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6f2f-381">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f2f-382">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6f2f-382">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6f2f-383">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6f2f-383">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f2f-384">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6f2f-384">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6f2f-385">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a6f2f-385">Namespace</span></span><br/>                | <span data-ttu-id="a6f2f-386">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a6f2f-386">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6f2f-387">MOF</span><span class="sxs-lookup"><span data-stu-id="a6f2f-387">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6f2f-388"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6f2f-388"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6f2f-389">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f2f-389">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6f2f-390"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6f2f-390"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f2f-391">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6f2f-391">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f2f-392">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a6f2f-392">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

