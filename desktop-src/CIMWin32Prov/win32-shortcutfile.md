---
description: Le \_ ShortcutFile Win32&\# 32 ; La classe WMI représente des fichiers qui sont des raccourcis vers d’autres fichiers, répertoires et commandes.
ms.assetid: 15973234-e418-4869-839e-a7c439512e4e
ms.tgt_platform: multiple
title: Classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile
- Win32_ShortcutFile.Caption
- Win32_ShortcutFile.Description
- Win32_ShortcutFile.InstallDate
- Win32_ShortcutFile.Status
- Win32_ShortcutFile.AccessMask
- Win32_ShortcutFile.Archive
- Win32_ShortcutFile.Compressed
- Win32_ShortcutFile.CompressionMethod
- Win32_ShortcutFile.CreationClassName
- Win32_ShortcutFile.CreationDate
- Win32_ShortcutFile.CSCreationClassName
- Win32_ShortcutFile.CSName
- Win32_ShortcutFile.Drive
- Win32_ShortcutFile.EightDotThreeFileName
- Win32_ShortcutFile.Encrypted
- Win32_ShortcutFile.EncryptionMethod
- Win32_ShortcutFile.Name
- Win32_ShortcutFile.Extension
- Win32_ShortcutFile.FileName
- Win32_ShortcutFile.FileSize
- Win32_ShortcutFile.FileType
- Win32_ShortcutFile.FSCreationClassName
- Win32_ShortcutFile.FSName
- Win32_ShortcutFile.Hidden
- Win32_ShortcutFile.InUseCount
- Win32_ShortcutFile.LastAccessed
- Win32_ShortcutFile.LastModified
- Win32_ShortcutFile.Path
- Win32_ShortcutFile.Readable
- Win32_ShortcutFile.System
- Win32_ShortcutFile.Writeable
- Win32_ShortcutFile.Manufacturer
- Win32_ShortcutFile.Version
- Win32_ShortcutFile.Target
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b714b4c8119f92931235734664726123744064d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514551"
---
# <a name="win32_shortcutfile-class"></a><span data-ttu-id="68ac6-103">\_Classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="68ac6-103">Win32\_ShortcutFile class</span></span>

<span data-ttu-id="68ac6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ShortcutFile** WMI représente des fichiers qui sont des raccourcis vers d’autres fichiers, répertoires et commandes.</span><span class="sxs-lookup"><span data-stu-id="68ac6-104">The **Win32\_ShortcutFile** [WMI class](../wmisdk/retrieving-a-class.md) represents files that are shortcuts to other files, directories, and commands.</span></span>

<span data-ttu-id="68ac6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="68ac6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68ac6-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="68ac6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ac6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68ac6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE466-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_ShortcutFile : CIM_DataFile
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
  string   Target;
};
```

## <a name="members"></a><span data-ttu-id="68ac6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="68ac6-108">Members</span></span>

<span data-ttu-id="68ac6-109">La classe **Win32 \_ ShortcutFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="68ac6-109">The **Win32\_ShortcutFile** class has these types of members:</span></span>

-   [<span data-ttu-id="68ac6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68ac6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="68ac6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68ac6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68ac6-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68ac6-112">Methods</span></span>

<span data-ttu-id="68ac6-113">La classe **Win32 \_ ShortcutFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="68ac6-113">The **Win32\_ShortcutFile** class has these methods.</span></span>



| <span data-ttu-id="68ac6-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="68ac6-114">Method</span></span>                                                                                                | <span data-ttu-id="68ac6-115">Description</span><span class="sxs-lookup"><span data-stu-id="68ac6-115">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68ac6-116">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="68ac6-116">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-shortcutfile.md)     | <span data-ttu-id="68ac6-117">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-117">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="68ac6-118">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-118">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-shortcutfile.md) | <span data-ttu-id="68ac6-119">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-119">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="68ac6-120">**Dens**</span><span class="sxs-lookup"><span data-stu-id="68ac6-120">**Compress**</span></span>](compress-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="68ac6-121">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-121">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="68ac6-122">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-122">**CompressEx**</span></span>](compressex-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="68ac6-123">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-123">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="68ac6-124">**Copier**</span><span class="sxs-lookup"><span data-stu-id="68ac6-124">**Copy**</span></span>](copy-method-in-class-win32-shortcutfile.md)                                               | <span data-ttu-id="68ac6-125">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="68ac6-125">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                     |
| [<span data-ttu-id="68ac6-126">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-126">**CopyEx**</span></span>](copyex-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="68ac6-127">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="68ac6-127">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                |
| [<span data-ttu-id="68ac6-128">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="68ac6-128">**Delete**</span></span>](delete-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="68ac6-129">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-129">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="68ac6-130">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-130">**DeleteEx**</span></span>](deleteex-method-in-class-win32-shortcutfile.md)                                       | <span data-ttu-id="68ac6-131">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-131">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="68ac6-132">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="68ac6-132">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-shortcutfile.md)           | <span data-ttu-id="68ac6-133">Méthode de classe qui détermine si l’appelant a les autorisations agrégées spécifiées par l’argument d’autorisation non seulement sur l’objet de fichier, mais sur le partage sur lequel le fichier ou le répertoire réside (s’il se trouve sur un partage).</span><span class="sxs-lookup"><span data-stu-id="68ac6-133">Class method that determines whether the caller has the aggregated permissions specified by the Permission argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="68ac6-134">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="68ac6-134">**Rename**</span></span>](rename-method-in-class-win32-shortcutfile.md)                                           | <span data-ttu-id="68ac6-135">Méthode de classe qui renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-135">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="68ac6-136">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="68ac6-136">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-shortcutfile.md)                             | <span data-ttu-id="68ac6-137">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-137">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="68ac6-138">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-138">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-shortcutfile.md)                         | <span data-ttu-id="68ac6-139">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-139">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="68ac6-140">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="68ac6-140">**Uncompress**</span></span>](uncompress-method-in-class-win32-shortcutfile.md)                                   | <span data-ttu-id="68ac6-141">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-141">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="68ac6-142">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="68ac6-142">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-shortcutfile.md)                               | <span data-ttu-id="68ac6-143">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-143">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="68ac6-144">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68ac6-144">Properties</span></span>

<span data-ttu-id="68ac6-145">La classe **Win32 \_ ShortcutFile** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="68ac6-145">The **Win32\_ShortcutFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68ac6-146">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="68ac6-146">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68ac6-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-149">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-149">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-150">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-150">Bitmask that represents the access rights required to access or perform specific operations on the file.</span></span> <span data-ttu-id="68ac6-151">Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](../wmisdk/file-and-directory-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-151">For bit values, see [**File and Directory Access Rights Constants**](../wmisdk/file-and-directory-access-rights-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="68ac6-152">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-152">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="68ac6-153">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-153">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="68ac6-154">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="68ac6-154">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="68ac6-155">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="68ac6-155">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="68ac6-156">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="68ac6-156">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="68ac6-157">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="68ac6-157">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="68ac6-158">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="68ac6-158">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="68ac6-159">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="68ac6-159">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="68ac6-160">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="68ac6-160">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="68ac6-161">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="68ac6-161">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="68ac6-162">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="68ac6-162">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="68ac6-163">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="68ac6-163">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="68ac6-164">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="68ac6-164">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="68ac6-165">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="68ac6-165">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="68ac6-166">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="68ac6-166">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="68ac6-167">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="68ac6-167">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68ac6-168">**Archive**</span><span class="sxs-lookup"><span data-stu-id="68ac6-168">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-169">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-171">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-171">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-172">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="68ac6-172">If **True**, the file should be archived.</span></span>

<span data-ttu-id="68ac6-173">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-173">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="68ac6-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-177">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-177">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-178">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-178">A short textual description of the object.</span></span>

<span data-ttu-id="68ac6-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-180">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="68ac6-180">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-181">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-183">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-183">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-184">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="68ac6-184">If **True**, the file is compressed.</span></span>

<span data-ttu-id="68ac6-185">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-185">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-186">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="68ac6-186">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-189">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-190">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="68ac6-190">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="68ac6-191">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-191">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="68ac6-192">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-192">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="68ac6-193">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-193">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="68ac6-194">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-194">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-198">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="68ac6-198">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-199">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="68ac6-199">Name of the class.</span></span>

<span data-ttu-id="68ac6-200">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-200">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-201">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="68ac6-201">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-202">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68ac6-202">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-204">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="68ac6-204">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-205">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-205">Date and time of the file's creation.</span></span>

<span data-ttu-id="68ac6-206">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-206">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-207">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-207">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-210">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="68ac6-210">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-211">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="68ac6-211">Class of the computer system.</span></span>

<span data-ttu-id="68ac6-212">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-213">**CSName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-213">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-216">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="68ac6-216">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-217">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="68ac6-217">Name of the computer system.</span></span>

<span data-ttu-id="68ac6-218">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-218">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-219">**Description**</span><span class="sxs-lookup"><span data-stu-id="68ac6-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-222">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="68ac6-222">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-223">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-223">A textual description of the object.</span></span>

<span data-ttu-id="68ac6-224">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-225">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="68ac6-225">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-226">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-228">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="68ac6-228">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-229">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-229">Drive letter (including the colon that follows the drive letter) of the file.</span></span>

<span data-ttu-id="68ac6-230">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="68ac6-230">Example: "c:"</span></span>

<span data-ttu-id="68ac6-231">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-231">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-232">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-232">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-235">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="68ac6-235">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-236">Nom de fichier au format 8,3.</span><span class="sxs-lookup"><span data-stu-id="68ac6-236">File name in 8.3 format.</span></span>

<span data-ttu-id="68ac6-237">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="68ac6-237">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="68ac6-238">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-238">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-239">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="68ac6-239">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-240">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-242">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="68ac6-242">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-243">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="68ac6-243">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="68ac6-244">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-244">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-245">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="68ac6-245">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-248">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-249">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="68ac6-249">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="68ac6-250">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-250">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="68ac6-251">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-251">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="68ac6-252">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-252">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="68ac6-253">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-254">**Extension**</span><span class="sxs-lookup"><span data-stu-id="68ac6-254">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-257">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="68ac6-257">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-258">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="68ac6-258">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="68ac6-259">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="68ac6-259">Example: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="68ac6-260">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-261">**FileName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-261">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-262">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-264">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file name")</span><span class="sxs-lookup"><span data-stu-id="68ac6-264">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-265">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-265">File name without the file name extension.</span></span>

<span data-ttu-id="68ac6-266">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="68ac6-266">Example: "MyDataFile"</span></span>

<span data-ttu-id="68ac6-267">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-267">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-268">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="68ac6-268">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68ac6-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-271">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Size »), [**Units**](../wmisdk/standard-qualifiers.md) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-271">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-272">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="68ac6-272">Size of the file, in bytes.</span></span>

<span data-ttu-id="68ac6-273">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-273">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="68ac6-274">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-274">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-275">**FileType**</span><span class="sxs-lookup"><span data-stu-id="68ac6-275">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-278">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="68ac6-278">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-279">Descripteur qui représente le type de fichier indiqué par la propriété d' **extension** .</span><span class="sxs-lookup"><span data-stu-id="68ac6-279">Descriptor that represents the file type indicated by the **Extension** property.</span></span>

<span data-ttu-id="68ac6-280">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-280">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-281">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-281">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-284">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="68ac6-284">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-285">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="68ac6-285">Class of the file system.</span></span>

<span data-ttu-id="68ac6-286">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-287">**FSName**</span><span class="sxs-lookup"><span data-stu-id="68ac6-287">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-290">Qualificateurs : [**propagés**](../wmisdk/standard-qualifiers.md) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="68ac6-290">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-291">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="68ac6-291">Name of the file system.</span></span>

<span data-ttu-id="68ac6-292">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-292">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-293">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="68ac6-293">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-294">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-296">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-297">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="68ac6-297">If **True**, the file is hidden.</span></span>

<span data-ttu-id="68ac6-298">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-298">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-299">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68ac6-299">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-300">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68ac6-300">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-302">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="68ac6-302">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-303">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="68ac6-303">Indicates when the object was installed.</span></span> <span data-ttu-id="68ac6-304">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="68ac6-304">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="68ac6-305">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-306">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="68ac6-306">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-307">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68ac6-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-309">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-310">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-310">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="68ac6-311">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-311">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="68ac6-312">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-312">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-313">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="68ac6-313">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-314">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68ac6-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-316">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-316">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-317">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-317">Date and time the file was last accessed.</span></span>

<span data-ttu-id="68ac6-318">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-318">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-319">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="68ac6-319">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-320">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68ac6-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-322">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-322">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-323">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="68ac6-323">Date and time the file was last modified.</span></span>

<span data-ttu-id="68ac6-324">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-324">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-325">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="68ac6-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-328">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="68ac6-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-329">Chaîne du fabricant de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="68ac6-329">Manufacturer string from the version resource (if one is present).</span></span>

<span data-ttu-id="68ac6-330">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-330">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-331">**Nom**</span><span class="sxs-lookup"><span data-stu-id="68ac6-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-332">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-334">Qualificateurs : [ **clé**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="68ac6-334">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-335">La propriété Name est une chaîne représentant le nom hérité qui sert de clé à une instance de fichier logique dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="68ac6-335">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="68ac6-336">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="68ac6-336">Full path names should be provided.</span></span>

<span data-ttu-id="68ac6-337">Exemple : C : \\ \\ système Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="68ac6-337">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="68ac6-338">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-338">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-339">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="68ac6-339">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-342">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("path")</span><span class="sxs-lookup"><span data-stu-id="68ac6-342">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-343">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="68ac6-343">Path of the file including the leading and trailing backslashes.</span></span>

<span data-ttu-id="68ac6-344">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="68ac6-344">Example: "\\windows\\system\\"</span></span>

<span data-ttu-id="68ac6-345">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-345">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-346">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="68ac6-346">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-347">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-347">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-349">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("readed")</span><span class="sxs-lookup"><span data-stu-id="68ac6-349">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-350">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="68ac6-350">If **True**, the file can be read.</span></span>

<span data-ttu-id="68ac6-351">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-352">**État**</span><span class="sxs-lookup"><span data-stu-id="68ac6-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-355">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="68ac6-355">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-356">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="68ac6-356">String that indicates the current status of the object.</span></span> <span data-ttu-id="68ac6-357">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="68ac6-357">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="68ac6-358">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-358">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="68ac6-359">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="68ac6-359">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="68ac6-360">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="68ac6-360">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68ac6-361">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="68ac6-361">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68ac6-362">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="68ac6-362">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68ac6-363">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-363">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68ac6-364">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="68ac6-364">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68ac6-365">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-365">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68ac6-366">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-366">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68ac6-367">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-367">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68ac6-368">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="68ac6-368">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68ac6-369">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-369">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68ac6-370">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-370">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68ac6-371">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-371">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68ac6-372">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-372">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68ac6-373">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-373">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68ac6-374">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-374">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68ac6-375">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-375">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68ac6-376">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-376">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68ac6-377">**Système**</span><span class="sxs-lookup"><span data-stu-id="68ac6-377">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-378">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-380">Qualificateurs : [**schéma**](../wmisdk/standard-qualifiers.md) (« Win32 »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-380">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-381">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="68ac6-381">If **True**, the file is a system file.</span></span>

<span data-ttu-id="68ac6-382">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-383">**Cible**</span><span class="sxs-lookup"><span data-stu-id="68ac6-383">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-384">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-386">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| \_ beginthreadex")</span><span class="sxs-lookup"><span data-stu-id="68ac6-386">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|\_beginthreadex")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-387">Nom de l’objet sur lequel il s’agit d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="68ac6-387">Name of the object that this is a shortcut to.</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-388">**Version**</span><span class="sxs-lookup"><span data-stu-id="68ac6-388">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-389">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="68ac6-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-391">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("version")</span><span class="sxs-lookup"><span data-stu-id="68ac6-391">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-392">Chaîne de version de la ressource de version (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="68ac6-392">Version string from the version resource (if one is present).</span></span>

<span data-ttu-id="68ac6-393">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-393">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="68ac6-394">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="68ac6-394">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68ac6-395">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="68ac6-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="68ac6-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68ac6-397">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="68ac6-397">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="68ac6-398">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="68ac6-398">If **True**, the file can be written.</span></span>

<span data-ttu-id="68ac6-399">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-399">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68ac6-400">Notes</span><span class="sxs-lookup"><span data-stu-id="68ac6-400">Remarks</span></span>

<span data-ttu-id="68ac6-401">La classe **Win32 \_ ShortcutFile** est dérivée du [**fichier de \_ fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="68ac6-401">The **Win32\_ShortcutFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68ac6-402">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68ac6-402">Requirements</span></span>



| <span data-ttu-id="68ac6-403">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68ac6-403">Requirement</span></span> | <span data-ttu-id="68ac6-404">Valeur</span><span class="sxs-lookup"><span data-stu-id="68ac6-404">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68ac6-405">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68ac6-405">Minimum supported client</span></span><br/> | <span data-ttu-id="68ac6-406">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68ac6-406">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68ac6-407">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68ac6-407">Minimum supported server</span></span><br/> | <span data-ttu-id="68ac6-408">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68ac6-408">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68ac6-409">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68ac6-409">Namespace</span></span><br/>                | <span data-ttu-id="68ac6-410">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="68ac6-410">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68ac6-411">MOF</span><span class="sxs-lookup"><span data-stu-id="68ac6-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68ac6-412"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68ac6-412"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68ac6-413">DLL</span><span class="sxs-lookup"><span data-stu-id="68ac6-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68ac6-414"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ac6-414"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ac6-415">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68ac6-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ac6-416">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="68ac6-416">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="68ac6-417">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="68ac6-417">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
