---
description: La \_ classe de fichier de données CIM représente une collection nommée de données ou du code exécutable. Seules les instances de fichiers sur des disques fixes locaux sont retournées.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: Classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861273"
---
# <a name="cim_datafile-class"></a><span data-ttu-id="6878a-104">\_Classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="6878a-104">CIM\_DataFile class</span></span>

<span data-ttu-id="6878a-105">La classe de **\_ fichier** de données CIM représente une collection nommée de données ou du code exécutable.</span><span class="sxs-lookup"><span data-stu-id="6878a-105">The **CIM\_DataFile** class represents a named collection of data or executable code.</span></span> <span data-ttu-id="6878a-106">Seules les instances de fichiers sur des disques fixes locaux sont retournées.</span><span class="sxs-lookup"><span data-stu-id="6878a-106">Only instances of files on local fixed disks will be returned.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6878a-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6878a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6878a-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6878a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6878a-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6878a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6878a-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6878a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6878a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6878a-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
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
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="6878a-112">Membres</span><span class="sxs-lookup"><span data-stu-id="6878a-112">Members</span></span>

<span data-ttu-id="6878a-113">La classe de **\_ fichier de fichier CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6878a-113">The **CIM\_DataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="6878a-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6878a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6878a-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6878a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6878a-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6878a-116">Methods</span></span>

<span data-ttu-id="6878a-117">La classe de **\_ fichier de fichier CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6878a-117">The **CIM\_DataFile** class has these methods.</span></span>



| <span data-ttu-id="6878a-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="6878a-118">Method</span></span>                                                                                          | <span data-ttu-id="6878a-119">Description</span><span class="sxs-lookup"><span data-stu-id="6878a-119">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6878a-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="6878a-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)     | <span data-ttu-id="6878a-121">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6878a-122">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-122">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6878a-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md) | <span data-ttu-id="6878a-124">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="6878a-125">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-125">Implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="6878a-126">**Dens**</span><span class="sxs-lookup"><span data-stu-id="6878a-126">**Compress**</span></span>](compress-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="6878a-127">Utilise la compression NTFS pour compresser le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-127">Uses NTFS compression to compress the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-128">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-128">Implemented by WMI.</span></span><br/>                       |
| [<span data-ttu-id="6878a-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-129">**CompressEx**</span></span>](compressex-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="6878a-130">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-131">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-131">Implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="6878a-132">**Copier**</span><span class="sxs-lookup"><span data-stu-id="6878a-132">**Copy**</span></span>](copy-method-in-class-cim-datafile.md)                                               | <span data-ttu-id="6878a-133">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6878a-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6878a-134">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-134">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6878a-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-135">**CopyEx**</span></span>](copyex-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6878a-136">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6878a-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="6878a-137">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-137">Implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="6878a-138">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="6878a-138">**Delete**</span></span>](delete-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6878a-139">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-140">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-140">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6878a-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-datafile.md)                                       | <span data-ttu-id="6878a-142">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-143">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-143">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6878a-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="6878a-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)           | <span data-ttu-id="6878a-145">Détermine si l’appelant dispose des autorisations agrégées spécifiées par l’argument d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="6878a-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="6878a-146">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-146">Implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="6878a-147">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="6878a-147">**Rename**</span></span>](rename-method-in-class-cim-datafile.md)                                           | <span data-ttu-id="6878a-148">Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-149">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-149">Implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="6878a-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="6878a-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-datafile.md)                             | <span data-ttu-id="6878a-151">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="6878a-152">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-152">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="6878a-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-datafile.md)                         | <span data-ttu-id="6878a-154">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="6878a-155">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-155">Implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="6878a-156">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="6878a-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-datafile.md)                                   | <span data-ttu-id="6878a-157">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-158">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-158">Implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="6878a-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="6878a-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-datafile.md)                               | <span data-ttu-id="6878a-160">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="6878a-161">Implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6878a-161">Implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="6878a-162">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6878a-162">Properties</span></span>

<span data-ttu-id="6878a-163">La classe de **\_ fichier de fichier CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6878a-163">The **CIM\_DataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6878a-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="6878a-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6878a-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-167">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="6878a-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-168">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-168">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="6878a-169">Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="6878a-169">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="6878a-170">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-170">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="6878a-171">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-171">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6878a-172">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="6878a-172">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="6878a-173">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="6878a-173">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="6878a-174">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="6878a-174">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="6878a-175">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="6878a-175">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="6878a-176">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="6878a-176">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="6878a-177">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="6878a-177">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="6878a-178">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="6878a-178">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="6878a-179">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="6878a-179">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="6878a-180">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="6878a-180">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="6878a-181">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="6878a-181">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="6878a-182">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="6878a-182">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="6878a-183">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="6878a-183">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="6878a-184">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="6878a-184">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="6878a-185">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="6878a-185">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6878a-186">**Archive**</span><span class="sxs-lookup"><span data-stu-id="6878a-186">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-187">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-189">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="6878a-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-190">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="6878a-190">If **True**, the file should be archived.</span></span>

<span data-ttu-id="6878a-191">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-191">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6878a-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-195">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6878a-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-196">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-196">A short textual description of the object.</span></span>

<span data-ttu-id="6878a-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-198">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="6878a-198">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-199">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-201">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="6878a-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-202">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="6878a-202">If **True**, the file is compressed.</span></span>

<span data-ttu-id="6878a-203">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-203">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-204">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="6878a-204">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-207">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="6878a-207">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-208">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6878a-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="6878a-209">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="6878a-209">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="6878a-210">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="6878a-210">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="6878a-211">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="6878a-211">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="6878a-212">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-213">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6878a-213">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-216">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="6878a-216">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-217">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="6878a-217">Name of the class.</span></span>

<span data-ttu-id="6878a-218">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-219">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="6878a-219">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-220">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6878a-220">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-222">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="6878a-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-223">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-223">Date and time of the file's creation.</span></span>

<span data-ttu-id="6878a-224">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-224">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-225">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6878a-225">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-226">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-228">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="6878a-228">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-229">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="6878a-229">Class of the computer system.</span></span>

<span data-ttu-id="6878a-230">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-230">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-231">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6878a-231">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-234">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="6878a-234">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-235">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="6878a-235">Name of the computer system.</span></span>

<span data-ttu-id="6878a-236">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-236">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-237">**Description**</span><span class="sxs-lookup"><span data-stu-id="6878a-237">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-240">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6878a-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-241">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-241">A textual description of the object.</span></span>

<span data-ttu-id="6878a-242">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-243">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="6878a-243">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-246">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="6878a-246">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-247">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-247">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="6878a-248">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="6878a-248">Example: "c:"</span></span>

<span data-ttu-id="6878a-249">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-249">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-250">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="6878a-250">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-253">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="6878a-253">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-254">Nom de fichier compatible DOS.</span><span class="sxs-lookup"><span data-stu-id="6878a-254">DOS-compatible file name.</span></span>

<span data-ttu-id="6878a-255">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="6878a-255">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="6878a-256">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-256">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-257">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="6878a-257">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-258">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-260">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="6878a-260">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-261">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="6878a-261">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="6878a-262">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-263">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="6878a-263">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-266">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="6878a-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-267">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6878a-267">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="6878a-268">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="6878a-268">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="6878a-269">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="6878a-269">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="6878a-270">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="6878a-270">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="6878a-271">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-271">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-272">**Extension**</span><span class="sxs-lookup"><span data-stu-id="6878a-272">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-275">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="6878a-275">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-276">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="6878a-276">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="6878a-277">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="6878a-277">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="6878a-278">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-278">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-279">**FileName**</span><span class="sxs-lookup"><span data-stu-id="6878a-279">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-282">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="6878a-282">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-283">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-283">File name without the file name extension.</span></span> <span data-ttu-id="6878a-284">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="6878a-284">Example: "MyDataFile"</span></span>

<span data-ttu-id="6878a-285">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-285">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-286">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="6878a-286">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-287">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6878a-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-289">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="6878a-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-290">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="6878a-290">Size of the file, in bytes.</span></span>

<span data-ttu-id="6878a-291">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6878a-291">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6878a-292">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-293">**FileType**</span><span class="sxs-lookup"><span data-stu-id="6878a-293">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-296">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="6878a-296">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-297">Descripteur qui représente le type de fichier indiqué par la propriété d' **extension** .</span><span class="sxs-lookup"><span data-stu-id="6878a-297">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="6878a-298">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-299">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6878a-299">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-302">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="6878a-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-303">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6878a-303">Class of the file system.</span></span>

<span data-ttu-id="6878a-304">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-304">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-305">**FSName**</span><span class="sxs-lookup"><span data-stu-id="6878a-305">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-308">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="6878a-308">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-309">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6878a-309">Name of the file system.</span></span>

<span data-ttu-id="6878a-310">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-311">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="6878a-311">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-312">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-314">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="6878a-314">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-315">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="6878a-315">If **True**, the file is hidden.</span></span>

<span data-ttu-id="6878a-316">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-316">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6878a-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-318">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6878a-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-320">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6878a-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-321">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="6878a-321">Indicates when the object was installed.</span></span> <span data-ttu-id="6878a-322">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="6878a-322">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6878a-323">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-324">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="6878a-324">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-325">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6878a-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-327">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="6878a-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-328">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-328">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="6878a-329">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6878a-329">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6878a-330">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-331">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="6878a-331">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-332">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6878a-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-334">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="6878a-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-335">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-335">Date and time the file was last accessed.</span></span>

<span data-ttu-id="6878a-336">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-337">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="6878a-337">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-338">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6878a-338">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-340">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="6878a-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-341">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-341">Date and time the file was last modified.</span></span>

<span data-ttu-id="6878a-342">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-342">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-343">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="6878a-343">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-346">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="6878a-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-347">Chaîne du fabricant de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="6878a-347">Manufacturer string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-348">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6878a-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-351">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6878a-351">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6878a-352">La propriété Name est une chaîne représentant le nom hérité qui sert de clé à une instance de fichier logique dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6878a-352">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="6878a-353">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="6878a-353">Full path names should be provided.</span></span>

<span data-ttu-id="6878a-354">Exemple : C : \\ \\ système Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="6878a-354">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="6878a-355">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-355">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-356">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="6878a-356">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-357">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-359">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="6878a-359">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-360">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="6878a-360">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="6878a-361">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="6878a-361">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="6878a-362">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-362">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-363">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="6878a-363">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-364">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-364">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-366">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="6878a-366">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-367">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="6878a-367">If **True**, the file can be read.</span></span>

<span data-ttu-id="6878a-368">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-368">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-369">**État**</span><span class="sxs-lookup"><span data-stu-id="6878a-369">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-372">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6878a-372">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-373">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6878a-373">String that indicates the current status of the object.</span></span> <span data-ttu-id="6878a-374">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="6878a-374">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6878a-375">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="6878a-375">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6878a-376">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="6878a-376">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6878a-377">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="6878a-377">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6878a-378">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="6878a-378">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6878a-379">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="6878a-379">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6878a-380">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6878a-381">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6878a-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6878a-382">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6878a-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6878a-383">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6878a-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6878a-384">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6878a-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6878a-385">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6878a-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6878a-386">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6878a-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6878a-387">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6878a-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6878a-388">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6878a-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6878a-389">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6878a-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6878a-390">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6878a-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6878a-391">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6878a-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6878a-392">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6878a-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6878a-393">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6878a-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6878a-394">**Système**</span><span class="sxs-lookup"><span data-stu-id="6878a-394">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-395">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-397">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="6878a-397">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-398">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="6878a-398">If **True**, the file is a system file.</span></span>

<span data-ttu-id="6878a-399">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-400">**Version**</span><span class="sxs-lookup"><span data-stu-id="6878a-400">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6878a-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-403">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("version")</span><span class="sxs-lookup"><span data-stu-id="6878a-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-404">Chaîne de version de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="6878a-404">Version string from the version resource (if one is present).</span></span>

</dd> <dt>

<span data-ttu-id="6878a-405">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="6878a-405">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6878a-406">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6878a-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6878a-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6878a-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6878a-408">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="6878a-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="6878a-409">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="6878a-409">If **True**, the file can be written.</span></span>

<span data-ttu-id="6878a-410">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6878a-411">Notes</span><span class="sxs-lookup"><span data-stu-id="6878a-411">Remarks</span></span>

<span data-ttu-id="6878a-412">La classe de **\_ fichier de fichier CIM** est dérivée de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6878a-412">The **CIM\_DataFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="6878a-413">WMI implémente la classe de **\_ fichier de fichier CIM** et toutes ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="6878a-413">WMI implements the **CIM\_DataFile** class and all of its methods.</span></span> <span data-ttu-id="6878a-414">La classe de **\_ fichier de fichier CIM** est une classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="6878a-414">The **CIM\_DataFile** class is a dynamic class.</span></span>

<span data-ttu-id="6878a-415">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6878a-415">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6878a-416">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6878a-416">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="6878a-417">En raison de la sécurité, WMI ne prend pas directement en charge l’appel d’un ordinateur distant et lui demande de copier des fichiers vers lui-même.</span><span class="sxs-lookup"><span data-stu-id="6878a-417">Due to security purposes, WMI does not directly support calling a remote computer and instructing it to copy files to itself.</span></span> <span data-ttu-id="6878a-418">Toutefois, vous pouvez utiliser le langage de programmation approprié pour appeler FTP ou RoboCopy, par exemple.</span><span class="sxs-lookup"><span data-stu-id="6878a-418">However, you can use the relevant programming language to call FTP or RoboCopy, for example.</span></span>

## <a name="examples"></a><span data-ttu-id="6878a-419">Exemples</span><span class="sxs-lookup"><span data-stu-id="6878a-419">Examples</span></span>

<span data-ttu-id="6878a-420">L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) du centre de script suivant utilise une classe de **fichier de \_ fichier CIM** dans le cadre d’une application plus volumineuse pour générer des rapports d’environnement Exchange à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6878a-420">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) uses a **CIM\_DataFile** class as part of a larger application to Generate exchange environment reports using Powershell.</span></span>

<span data-ttu-id="6878a-421">L’exemple de code [Rechercher des fichiers avec WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) dans la Galerie TechNet utilise un **fichier de \_ fichier CIM** pour rechercher un ou plusieurs fichiers sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6878a-421">The [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) code sample in TechNet Gallery uses a **CIM\_DataFile** to search for one or more files across multiple computers.</span></span>

<span data-ttu-id="6878a-422">L’exemple de code VBS suivant décrit comment effectuer une recherche par caractères génériques standard sur un fichier de fichier.</span><span class="sxs-lookup"><span data-stu-id="6878a-422">The following VBS code sample describes how to perform a standard wildcard search on a datafile.</span></span> <span data-ttu-id="6878a-423">Notez que les séparateurs de la barre oblique inverse doivent être placés dans une séquence d’échappement avec une autre barre oblique inverse ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="6878a-423">Note that the backslash delimiters must be escaped with another backslash (\\\\).</span></span> <span data-ttu-id="6878a-424">En outre, lors de l’utilisation de «**\_ fichier de fichier CIM**.**FileName**» dans la clause WHERE, le processus Wmiprvse analyse tous les répertoires sur les périphériques de stockage disponibles.</span><span class="sxs-lookup"><span data-stu-id="6878a-424">Also, when using "**CIM\_DataFile**.**FileName**" in the WHERE clause, the WMIPRVSE process will scan all directories on any available storage device.</span></span> <span data-ttu-id="6878a-425">Cela peut prendre un certain temps, surtout si vous avez mappé des partages distants et peut déclencher des avertissements antivirus.</span><span class="sxs-lookup"><span data-stu-id="6878a-425">This may take some time, especially if you have mapped remote shares, and can trigger antivirus warnings.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



<span data-ttu-id="6878a-426">L’extrait de code suivant limite la plage de recherche à un lecteur, un chemin d’accès et une extension de fichier spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6878a-426">The following snippet limits the search range to a specific drive, path, and file extension.</span></span>


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



<span data-ttu-id="6878a-427">L’exemple de code PowerShell suivant récupère une valeur d’attribut unique.</span><span class="sxs-lookup"><span data-stu-id="6878a-427">The following PowerShell code sample retrieves a single attribute value.</span></span>


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



## <a name="requirements"></a><span data-ttu-id="6878a-428">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6878a-428">Requirements</span></span>



| <span data-ttu-id="6878a-429">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6878a-429">Requirement</span></span> | <span data-ttu-id="6878a-430">Valeur</span><span class="sxs-lookup"><span data-stu-id="6878a-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6878a-431">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6878a-431">Minimum supported client</span></span><br/> | <span data-ttu-id="6878a-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6878a-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6878a-433">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6878a-433">Minimum supported server</span></span><br/> | <span data-ttu-id="6878a-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6878a-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6878a-435">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6878a-435">Namespace</span></span><br/>                | <span data-ttu-id="6878a-436">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6878a-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6878a-437">MOF</span><span class="sxs-lookup"><span data-stu-id="6878a-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6878a-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6878a-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6878a-439">DLL</span><span class="sxs-lookup"><span data-stu-id="6878a-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6878a-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6878a-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6878a-441">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6878a-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6878a-442">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="6878a-442">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="6878a-443">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="6878a-443">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="6878a-444">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="6878a-444">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

