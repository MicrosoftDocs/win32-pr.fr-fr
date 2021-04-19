---
description: Le \_ fichier d’échange Win32&\# 32 ; La classe WMI représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système Win32. Cette classe a été déconseillée.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513949"
---
# <a name="win32_pagefile-class"></a><span data-ttu-id="701f5-104">\_Classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="701f5-104">Win32\_PageFile class</span></span>

<span data-ttu-id="701f5-105">La [classe WMI](../wmisdk/retrieving-a-class.md) du fichier d' **\_ échange Win32** représente le fichier utilisé pour gérer l’échange de fichiers de mémoire virtuelle sur un système Win32.</span><span class="sxs-lookup"><span data-stu-id="701f5-105">The **Win32\_PageFile** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="701f5-106">Cette classe a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="701f5-106">This class has been deprecated.</span></span>

<span data-ttu-id="701f5-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="701f5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="701f5-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="701f5-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="701f5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="701f5-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="701f5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="701f5-110">Members</span></span>

<span data-ttu-id="701f5-111">La classe du **\_ fichier d’échange Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="701f5-111">The **Win32\_PageFile** class has these types of members:</span></span>

-   [<span data-ttu-id="701f5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="701f5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="701f5-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="701f5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="701f5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="701f5-114">Methods</span></span>

<span data-ttu-id="701f5-115">La **classe \_ pagefile Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="701f5-115">The **Win32\_PageFile** class has these methods.</span></span>



| <span data-ttu-id="701f5-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="701f5-116">Method</span></span>                                                                                            | <span data-ttu-id="701f5-117">Description</span><span class="sxs-lookup"><span data-stu-id="701f5-117">Description</span></span>                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701f5-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="701f5-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-pagefile.md)     | <span data-ttu-id="701f5-119">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="701f5-120">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-120">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | <span data-ttu-id="701f5-121">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-121">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="701f5-122">**Dens**</span><span class="sxs-lookup"><span data-stu-id="701f5-122">**Compress**</span></span>](compress-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="701f5-123">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="701f5-124">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-124">**CompressEx**</span></span>](compressex-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="701f5-125">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-125">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="701f5-126">**Copier**</span><span class="sxs-lookup"><span data-stu-id="701f5-126">**Copy**</span></span>](copy-method-in-class-win32-pagefile.md)                                               | <span data-ttu-id="701f5-127">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="701f5-127">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                       |
| [<span data-ttu-id="701f5-128">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-128">**CopyEx**</span></span>](copyex-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="701f5-129">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName.</span><span class="sxs-lookup"><span data-stu-id="701f5-129">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                                    |
| [<span data-ttu-id="701f5-130">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="701f5-130">**Delete**</span></span>](delete-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="701f5-131">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="701f5-132">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-132">**DeleteEx**</span></span>](deleteex-method-in-class-win32-pagefile.md)                                       | <span data-ttu-id="701f5-133">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-133">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="701f5-134">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="701f5-134">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-pagefile.md)           | <span data-ttu-id="701f5-135">Méthode de classe qui détermine si l’appelant a les autorisations agrégées spécifiées par l’argument d' *autorisation* non seulement sur l’objet de fichier, mais sur le partage sur lequel le fichier ou le répertoire réside (s’il se trouve sur un partage).</span><span class="sxs-lookup"><span data-stu-id="701f5-135">Class method that determines whether the caller has the aggregated permissions specified by the *Permission* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="701f5-136">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="701f5-136">**Rename**</span></span>](rename-method-in-class-win32-pagefile.md)                                           | <span data-ttu-id="701f5-137">Méthode de classe qui renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-137">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="701f5-138">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="701f5-138">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-pagefile.md)                             | <span data-ttu-id="701f5-139">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="701f5-140">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-140">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-pagefile.md)                         | <span data-ttu-id="701f5-141">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-141">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="701f5-142">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="701f5-142">**Uncompress**</span></span>](uncompress-method-in-class-win32-pagefile.md)                                   | <span data-ttu-id="701f5-143">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="701f5-144">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="701f5-144">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-pagefile.md)                               | <span data-ttu-id="701f5-145">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-145">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="701f5-146">Propriétés</span><span class="sxs-lookup"><span data-stu-id="701f5-146">Properties</span></span>

<span data-ttu-id="701f5-147">La classe du **\_ fichier d’échange Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="701f5-147">The **Win32\_PageFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="701f5-148">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="701f5-148">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="701f5-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-151">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="701f5-151">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-152">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-152">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="701f5-153">Pour obtenir les valeurs, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-153">For values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

<span data-ttu-id="701f5-154">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-154">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="701f5-155">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="701f5-155">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="701f5-156">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="701f5-156">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="701f5-157">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="701f5-157">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="701f5-158">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="701f5-158">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="701f5-159">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="701f5-159">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="701f5-160">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="701f5-160">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="701f5-161">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="701f5-161">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="701f5-162">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="701f5-162">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="701f5-163">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="701f5-163">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="701f5-164">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="701f5-164">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="701f5-165">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="701f5-165">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="701f5-166">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="701f5-166">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="701f5-167">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="701f5-167">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="701f5-168">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="701f5-168">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="701f5-169">**Archive**</span><span class="sxs-lookup"><span data-stu-id="701f5-169">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-172">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="701f5-172">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-173">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="701f5-173">If **True**, the file should be archived.</span></span>

<span data-ttu-id="701f5-174">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-174">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="701f5-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-178">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="701f5-178">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-179">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-179">A short textual description of the object.</span></span>

<span data-ttu-id="701f5-180">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-181">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="701f5-181">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-182">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-184">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="701f5-184">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-185">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="701f5-185">If **True**, the file is compressed.</span></span>

<span data-ttu-id="701f5-186">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-186">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-187">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="701f5-187">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-190">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="701f5-190">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-191">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="701f5-191">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="701f5-192">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="701f5-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="701f5-193">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="701f5-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="701f5-194">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="701f5-194">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="701f5-195">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="701f5-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-199">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="701f5-199">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-200">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="701f5-200">Name of the class.</span></span>

<span data-ttu-id="701f5-201">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-202">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="701f5-202">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-203">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="701f5-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-205">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="701f5-205">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-206">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-206">Date and time of the file's creation.</span></span>

<span data-ttu-id="701f5-207">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-207">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-208">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="701f5-208">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-211">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="701f5-211">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-212">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="701f5-212">Class of the computer system.</span></span>

<span data-ttu-id="701f5-213">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-213">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-214">**CSName**</span><span class="sxs-lookup"><span data-stu-id="701f5-214">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-217">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="701f5-217">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-218">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="701f5-218">Name of the computer system.</span></span>

<span data-ttu-id="701f5-219">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-220">**Description**</span><span class="sxs-lookup"><span data-stu-id="701f5-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-223">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="701f5-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-224">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-224">A textual description of the object.</span></span>

<span data-ttu-id="701f5-225">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-226">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="701f5-226">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-229">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="701f5-229">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-230">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-230">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="701f5-231">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="701f5-232">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="701f5-232">Example: "c:"</span></span>

<span data-ttu-id="701f5-233">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-234">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="701f5-234">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-237">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="701f5-237">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-238">Nom de fichier compatible DOS.</span><span class="sxs-lookup"><span data-stu-id="701f5-238">DOS-compatible file name.</span></span>

<span data-ttu-id="701f5-239">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="701f5-239">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="701f5-240">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-240">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-241">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="701f5-241">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-242">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-244">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="701f5-244">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-245">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="701f5-245">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="701f5-246">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-247">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="701f5-247">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-250">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="701f5-250">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-251">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="701f5-251">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="701f5-252">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="701f5-252">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="701f5-253">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="701f5-253">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="701f5-254">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="701f5-254">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="701f5-255">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-256">**Extension**</span><span class="sxs-lookup"><span data-stu-id="701f5-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-259">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="701f5-259">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-260">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="701f5-260">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="701f5-261">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="701f5-261">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="701f5-262">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-262">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="701f5-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-266">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file name")</span><span class="sxs-lookup"><span data-stu-id="701f5-266">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-267">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-267">File name without the file name extension.</span></span> <span data-ttu-id="701f5-268">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="701f5-268">Example: "MyDataFile"</span></span>

<span data-ttu-id="701f5-269">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="701f5-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-271">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="701f5-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-273">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Size »), [**Units**](../wmisdk/standard-qualifiers.md) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="701f5-273">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-274">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="701f5-274">Size of the file, in bytes.</span></span>

<span data-ttu-id="701f5-275">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="701f5-275">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="701f5-276">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-276">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="701f5-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-280">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="701f5-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-281">Descripteur qui représente le type de fichier indiqué par la propriété d' **extension** .</span><span class="sxs-lookup"><span data-stu-id="701f5-281">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="701f5-282">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-283">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="701f5-283">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-284">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="701f5-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-286">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| gestion de mémoire \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unités**](../wmisdk/standard-qualifiers.md) ("mégaoctets")</span><span class="sxs-lookup"><span data-stu-id="701f5-286">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwAvailPageFile"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-287">Espace disponible dans le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="701f5-287">Space available in the paging file.</span></span> <span data-ttu-id="701f5-288">Le système d’exploitation peut agrandir le fichier d’échange en fonction des besoins, jusqu’à la limite imposée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="701f5-288">The operating system can enlarge the paging file as necessary, up to the limit imposed by the user.</span></span> <span data-ttu-id="701f5-289">Cette propriété indique la différence entre la taille de la mémoire actuellement validée et la taille actuelle du fichier d’échange. elle n’affiche pas la plus grande taille possible du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="701f5-289">This property shows the difference between the size of current committed memory and the current size of the paging file; it does not show the largest possible size of the paging file.</span></span>

</dd> <dt>

<span data-ttu-id="701f5-290">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="701f5-290">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-291">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-293">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="701f5-293">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-294">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="701f5-294">Class of the file system.</span></span>

<span data-ttu-id="701f5-295">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-295">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-296">**FSName**</span><span class="sxs-lookup"><span data-stu-id="701f5-296">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-299">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="701f5-299">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-300">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="701f5-300">Name of the file system.</span></span>

<span data-ttu-id="701f5-301">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-302">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="701f5-302">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-303">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-305">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="701f5-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-306">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="701f5-306">If **True**, the file is hidden.</span></span>

<span data-ttu-id="701f5-307">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-307">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-308">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="701f5-308">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-309">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="701f5-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-311">Qualificateurs : [**déconseillé**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| PagingFiles »), [**Units**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="701f5-311">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-312">Taille initiale du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="701f5-312">Initial size of the page file.</span></span>

</dd> <dt>

<span data-ttu-id="701f5-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="701f5-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-314">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="701f5-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-316">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="701f5-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-317">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="701f5-317">Indicates when the object was installed.</span></span> <span data-ttu-id="701f5-318">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="701f5-318">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="701f5-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-320">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="701f5-320">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-321">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="701f5-321">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-323">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="701f5-323">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-324">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-324">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="701f5-325">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="701f5-325">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="701f5-326">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-326">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-327">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="701f5-327">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-328">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="701f5-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-330">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="701f5-330">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-331">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-331">Date and time the file was last accessed.</span></span>

<span data-ttu-id="701f5-332">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-332">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-333">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="701f5-333">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-334">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="701f5-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-336">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="701f5-336">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-337">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="701f5-337">Date and time the file was last modified.</span></span>

<span data-ttu-id="701f5-338">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-339">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="701f5-339">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-342">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="701f5-342">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-343">Chaîne du fabricant de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="701f5-343">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="701f5-344">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-344">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-345">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="701f5-345">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-346">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="701f5-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-348">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| gestion de mémoire \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unités**](../wmisdk/standard-qualifiers.md) ("mégaoctets")</span><span class="sxs-lookup"><span data-stu-id="701f5-348">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-349">Taille maximale du fichier d’échange, définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="701f5-349">Maximum size of the page file as set by the user.</span></span> <span data-ttu-id="701f5-350">Le système d’exploitation ne permet pas au fichier d’échange de dépasser cette limite.</span><span class="sxs-lookup"><span data-stu-id="701f5-350">The operating system will not allow the page file to exceed this limit.</span></span>

</dd> <dt>

<span data-ttu-id="701f5-351">**Nom**</span><span class="sxs-lookup"><span data-stu-id="701f5-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-354">Qualificateurs : [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName")</span><span class="sxs-lookup"><span data-stu-id="701f5-354">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemPageFileInformation\|PageFileName")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-355">Nom du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="701f5-355">Name of the page file.</span></span>

<span data-ttu-id="701f5-356">Exemple : « C : \\PAGEFILE.SYS »</span><span class="sxs-lookup"><span data-stu-id="701f5-356">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="701f5-357">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="701f5-357">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-360">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("path")</span><span class="sxs-lookup"><span data-stu-id="701f5-360">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-361">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="701f5-361">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="701f5-362">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="701f5-362">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="701f5-363">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-363">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-364">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="701f5-364">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-365">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-365">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-367">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("readed")</span><span class="sxs-lookup"><span data-stu-id="701f5-367">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-368">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="701f5-368">If **True**, the file can be read.</span></span>

<span data-ttu-id="701f5-369">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-369">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-370">**État**</span><span class="sxs-lookup"><span data-stu-id="701f5-370">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-373">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="701f5-373">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-374">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="701f5-374">String that indicates the current status of the object.</span></span>

<span data-ttu-id="701f5-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="701f5-376">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="701f5-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="701f5-377">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="701f5-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="701f5-378">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="701f5-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="701f5-379">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="701f5-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="701f5-380">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="701f5-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="701f5-381">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="701f5-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="701f5-382">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="701f5-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="701f5-383">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="701f5-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="701f5-384">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="701f5-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="701f5-385">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="701f5-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="701f5-386">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="701f5-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="701f5-387">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="701f5-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="701f5-388">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="701f5-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="701f5-389">**Système**</span><span class="sxs-lookup"><span data-stu-id="701f5-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-390">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-392">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="701f5-392">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-393">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="701f5-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="701f5-394">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="701f5-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-396">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="701f5-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-398">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("version")</span><span class="sxs-lookup"><span data-stu-id="701f5-398">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-399">Chaîne de version de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="701f5-399">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="701f5-400">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="701f5-401">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="701f5-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701f5-402">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="701f5-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701f5-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="701f5-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701f5-404">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="701f5-404">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="701f5-405">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="701f5-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="701f5-406">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="701f5-407">Notes</span><span class="sxs-lookup"><span data-stu-id="701f5-407">Remarks</span></span>

<span data-ttu-id="701f5-408">La classe du **\_ fichier d’échange Win32** est dérivée du [**\_ répertoire CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="701f5-408">The **Win32\_PageFile** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="701f5-409">Exemples</span><span class="sxs-lookup"><span data-stu-id="701f5-409">Examples</span></span>

<span data-ttu-id="701f5-410">L’exemple de code VBScript suivant montre comment récupérer des statistiques de fichier d’échange à partir d’instances du fichier d' **\_ échange Win32**.</span><span class="sxs-lookup"><span data-stu-id="701f5-410">The following VBScript code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



<span data-ttu-id="701f5-411">L’exemple de code perl suivant montre comment récupérer des statistiques de fichier d’échange à partir d’instances du fichier d' **\_ échange Win32**.</span><span class="sxs-lookup"><span data-stu-id="701f5-411">The following Perl code sample demonstrates how to retrieve page file stats from instances of **Win32\_PageFile**.</span></span>


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="701f5-412">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="701f5-412">Requirements</span></span>



| <span data-ttu-id="701f5-413">Condition requise</span><span class="sxs-lookup"><span data-stu-id="701f5-413">Requirement</span></span> | <span data-ttu-id="701f5-414">Valeur</span><span class="sxs-lookup"><span data-stu-id="701f5-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="701f5-415">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="701f5-415">Minimum supported client</span></span><br/> | <span data-ttu-id="701f5-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="701f5-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="701f5-417">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="701f5-417">Minimum supported server</span></span><br/> | <span data-ttu-id="701f5-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="701f5-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="701f5-419">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="701f5-419">Namespace</span></span><br/>                | <span data-ttu-id="701f5-420">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="701f5-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="701f5-421">MOF</span><span class="sxs-lookup"><span data-stu-id="701f5-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="701f5-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="701f5-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="701f5-423">DLL</span><span class="sxs-lookup"><span data-stu-id="701f5-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="701f5-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="701f5-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="701f5-425">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="701f5-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701f5-426">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="701f5-426">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="701f5-427">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="701f5-427">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
