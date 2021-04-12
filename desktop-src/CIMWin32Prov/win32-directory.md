---
description: Répertoire Win32 \_&\# 32 ; La classe WMI représente une entrée de répertoire sur un système informatique exécutant Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201084"
---
# <a name="win32_directory-class"></a><span data-ttu-id="13760-103">\_Classe de répertoire Win32</span><span class="sxs-lookup"><span data-stu-id="13760-103">Win32\_Directory class</span></span>

<span data-ttu-id="13760-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l' **\_ Annuaire Win32** représente une entrée de répertoire sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="13760-104">The **Win32\_Directory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a directory entry on a computer system running Windows.</span></span> <span data-ttu-id="13760-105">Un répertoire est un type de fichier qui regroupe logiquement des fichiers de données et fournit des informations de chemin d’accès pour les fichiers groupés.</span><span class="sxs-lookup"><span data-stu-id="13760-105">A directory is a type of file that logically groups data files and provides path information for the grouped files.</span></span> <span data-ttu-id="13760-106">Exemple : C : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="13760-106">Example: C:\\TEMP.</span></span> <span data-ttu-id="13760-107">**Win32 \_ Le répertoire** n’inclut pas les répertoires des lecteurs réseau.</span><span class="sxs-lookup"><span data-stu-id="13760-107">**Win32\_Directory** does not include directories of network drives.</span></span>

<span data-ttu-id="13760-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="13760-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="13760-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="13760-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13760-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13760-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="13760-111">Membres</span><span class="sxs-lookup"><span data-stu-id="13760-111">Members</span></span>

<span data-ttu-id="13760-112">La classe de **\_ répertoire win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="13760-112">The **Win32\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="13760-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="13760-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="13760-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13760-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13760-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="13760-115">Methods</span></span>

<span data-ttu-id="13760-116">La classe de **\_ répertoire win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="13760-116">The **Win32\_Directory** class has these methods.</span></span>



| <span data-ttu-id="13760-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="13760-117">Method</span></span>                                                                                             | <span data-ttu-id="13760-118">Description</span><span class="sxs-lookup"><span data-stu-id="13760-118">Description</span></span>                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13760-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="13760-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-directory.md)     | <span data-ttu-id="13760-120">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-120">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="13760-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="13760-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-directory.md) | <span data-ttu-id="13760-122">Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-122">Class method that changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="13760-123">**Dens**</span><span class="sxs-lookup"><span data-stu-id="13760-123">**Compress**</span></span>](compress-method-in-class-win32-directory.md)                                       | <span data-ttu-id="13760-124">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-124">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="13760-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="13760-125">**CompressEx**</span></span>](compressex-method-in-class-win32-directory.md)                                   | <span data-ttu-id="13760-126">Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-126">Class method that compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="13760-127">**Copier**</span><span class="sxs-lookup"><span data-stu-id="13760-127">**Copy**</span></span>](copy-method-in-class-win32-directory.md)                                               | <span data-ttu-id="13760-128">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="13760-128">Class method that copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                        |
| [<span data-ttu-id="13760-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="13760-129">**CopyEx**</span></span>](copyex-method-in-class-win32-directory.md)                                           | <span data-ttu-id="13760-130">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="13760-130">Class method that copies the logical file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span><br/>                                                                                   |
| [<span data-ttu-id="13760-131">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="13760-131">**Delete**</span></span>](delete-method-in-class-win32-directory.md)                                           | <span data-ttu-id="13760-132">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-132">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="13760-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="13760-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-directory.md)                                       | <span data-ttu-id="13760-134">Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-134">Class method that deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="13760-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="13760-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-directory.md)           | <span data-ttu-id="13760-136">Méthode de classe qui détermine si l’appelant a les autorisations agrégées spécifiées par l’argument d' *autorisation* non seulement sur l’objet de fichier, mais sur le partage sur lequel le fichier ou le répertoire réside (s’il se trouve sur un partage).</span><span class="sxs-lookup"><span data-stu-id="13760-136">Class method that determines whether the caller has the aggregated permissions specified by the *Permissions* argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="13760-137">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="13760-137">**Rename**</span></span>](rename-method-in-class-win32-directory.md)                                           | <span data-ttu-id="13760-138">Méthode de classe qui renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="13760-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="13760-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-directory.md)                             | <span data-ttu-id="13760-140">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-140">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="13760-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="13760-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-directory.md)                         | <span data-ttu-id="13760-142">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="13760-143">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="13760-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)                                   | <span data-ttu-id="13760-144">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-144">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="13760-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="13760-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-directory.md)                               | <span data-ttu-id="13760-146">Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-146">Class method that uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="13760-147">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13760-147">Properties</span></span>

<span data-ttu-id="13760-148">La classe de **\_ répertoire win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="13760-148">The **Win32\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13760-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="13760-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13760-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13760-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-152">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="13760-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="13760-153">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="13760-153">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="13760-154">Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="13760-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="13760-155">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="13760-156">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="13760-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="13760-157"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13760-158">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-158">Grants the right to read data from the file.</span></span> <span data-ttu-id="13760-159">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="13760-159">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="13760-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="13760-160"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13760-161">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-161">Grants the right to write data to the file.</span></span> <span data-ttu-id="13760-162">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="13760-162">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="13760-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Fichier \_ Ajouter des \_ données (fichier) ou \_ un \_ sous-répertoire d’ajout de fichier** (4)</span><span class="sxs-lookup"><span data-stu-id="13760-163"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13760-164">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-164">Grants the right to append data to the file.</span></span> <span data-ttu-id="13760-165">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="13760-165">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="13760-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="13760-166"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="13760-167">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="13760-167">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="13760-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="13760-168"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="13760-169">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="13760-169">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="13760-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="13760-170"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="13760-171">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-171">Grants the right to execute a file.</span></span> <span data-ttu-id="13760-172">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="13760-172">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="13760-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="13760-173"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="13760-174">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="13760-174">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="13760-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="13760-175"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="13760-176">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-176">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="13760-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="13760-177"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="13760-178">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-178">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="13760-179"><span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="13760-179"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="13760-180">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="13760-180">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="13760-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="13760-181"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="13760-182">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="13760-182">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="13760-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="13760-183"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="13760-184">Octroie l’accès en écriture à la liste de contrôle d’accès discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="13760-184">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="13760-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="13760-185"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="13760-186">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="13760-186">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="13760-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="13760-187"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="13760-188">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="13760-188">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span data-ttu-id="13760-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Accès \_ \_Sécurité du système** (18809343)</span><span class="sxs-lookup"><span data-stu-id="13760-189"><span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**ACCESS\_SYSTEM\_SECURITY** (18809343)</span></span>


</dt> <dd>

<span data-ttu-id="13760-190">Contrôle la capacité à récupérer ou à définir la liste SACL dans le descripteur de sécurité d’un objet.</span><span class="sxs-lookup"><span data-stu-id="13760-190">Controls the ability to get or set the SACL in an object's security descriptor.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13760-191">**Archive**</span><span class="sxs-lookup"><span data-stu-id="13760-191">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-192">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-194">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="13760-194">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="13760-195">Indique si le bit d’archive sur le dossier a été défini.</span><span class="sxs-lookup"><span data-stu-id="13760-195">Indicates whether the archive bit on the folder has been set.</span></span> <span data-ttu-id="13760-196">Le bit d’archive est utilisé par les programmes de sauvegarde pour identifier les fichiers qui doivent être sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="13760-196">The archive bit is used by backup programs to identify files that should be backed up.</span></span> <span data-ttu-id="13760-197">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="13760-197">If **True**, the file should be archived.</span></span>

<span data-ttu-id="13760-198">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-198">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="13760-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-200">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-202">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="13760-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="13760-203">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-203">A short textual description of the object.</span></span>

<span data-ttu-id="13760-204">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13760-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-205">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="13760-205">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-206">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-208">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="13760-208">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="13760-209">Indique si le dossier a été compressé ou non.</span><span class="sxs-lookup"><span data-stu-id="13760-209">Indicates whether or not the folder has been compressed.</span></span> <span data-ttu-id="13760-210">WMI reconnaît les dossiers compressés à l’aide de WMI lui-même ou à l’aide de l’interface utilisateur graphique ; Toutefois, elle ne reconnaît pas. Fichiers ZIP en cours de compression.</span><span class="sxs-lookup"><span data-stu-id="13760-210">WMI recognizes folders compressed using WMI itself or using the graphical user interface; it does not, however, recognize .ZIP files as being compressed.</span></span> <span data-ttu-id="13760-211">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="13760-211">If **True**, the file is compressed.</span></span>

<span data-ttu-id="13760-212">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-212">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-213">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="13760-213">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-216">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="13760-216">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="13760-217">Algorithme ou outil (généralement une méthode) utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="13760-217">Algorithm or tool (usually a method) used to compress the logical file.</span></span> <span data-ttu-id="13760-218">Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez les mots suivants : « inconnu » pour indiquer qu’il n’est pas connu que le fichier logique est compressé ou non ; « Compressed » pour représenter le fait que le fichier est compressé, mais que son schéma de compression n’est pas connu ou qu’il n’est pas divulgué ; et « non compressés » pour indiquer que le fichier logique n’est pas compressé.</span><span class="sxs-lookup"><span data-stu-id="13760-218">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed; "Compressed" to represent that the file is compressed, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="13760-219">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-219">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-220">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13760-220">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-223">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="13760-223">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-224">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="13760-224">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="13760-225">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="13760-225">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="13760-226">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-226">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-227">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="13760-227">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-228">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13760-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13760-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-230">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="13760-230">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="13760-231">Date à laquelle l’objet système de fichiers a été créé.</span><span class="sxs-lookup"><span data-stu-id="13760-231">Date that the file system object was created.</span></span> <span data-ttu-id="13760-232">Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="13760-232">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="13760-233">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-233">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-234">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13760-234">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-237">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="13760-237">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-238">Nom de la classe de création du système d’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="13760-238">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="13760-239">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-239">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-240">**CSName**</span><span class="sxs-lookup"><span data-stu-id="13760-240">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-243">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="13760-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-244">Nom de l’ordinateur où est stocké l’objet de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-244">Name of the computer where the file system object is stored.</span></span>

<span data-ttu-id="13760-245">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-245">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-246">**Description**</span><span class="sxs-lookup"><span data-stu-id="13760-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-249">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="13760-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="13760-250">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-250">A textual description of the object.</span></span>

<span data-ttu-id="13760-251">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13760-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-252">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="13760-252">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-255">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="13760-255">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="13760-256">Lettre de lecteur du lecteur (y compris les deux-points) dans laquelle l’objet de système de fichiers est stocké.</span><span class="sxs-lookup"><span data-stu-id="13760-256">Drive letter of the drive (including colon) where the file system object is stored.</span></span>

<span data-ttu-id="13760-257">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="13760-257">Example: "c:"</span></span>

<span data-ttu-id="13760-258">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-258">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-259">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="13760-259">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-262">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="13760-262">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-263">Nom compatible MS-DOS pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-263">MS-DOS -compatible name for the folder.</span></span>

<span data-ttu-id="13760-264">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="13760-264">Example: "c:\\progra~1"</span></span>

<span data-ttu-id="13760-265">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-266">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="13760-266">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-267">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-269">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="13760-269">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="13760-270">Indique si le dossier a été chiffré ou non.</span><span class="sxs-lookup"><span data-stu-id="13760-270">Indicates whether or not the folder has been encrypted.</span></span> <span data-ttu-id="13760-271">Si la **valeur est true**, le dossier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="13760-271">If **True**, the folder is encrypted.</span></span>

<span data-ttu-id="13760-272">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-273">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="13760-273">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-276">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="13760-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="13760-277">Algorithme ou outil utilisé pour chiffrer le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="13760-277">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="13760-278">Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de chiffrement (pour des raisons de sécurité, par exemple), utilisez les mots suivants : « inconnu » pour indiquer qu’il est impossible de savoir si le fichier logique est chiffré ; « Chiffré » pour représenter le chiffrement du fichier, mais son schéma de chiffrement n’est pas connu ou n’est pas divulgué ; et « non chiffrés » pour représenter le fait que le fichier logique n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="13760-278">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted; "Encrypted" to represent that the file is encrypted, but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="13760-279">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-280">**Extension**</span><span class="sxs-lookup"><span data-stu-id="13760-280">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-283">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="13760-283">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="13760-284">Extension de nom de fichier pour l’objet de système de fichiers, à l’exclusion du point (.) qui sépare l’extension du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-284">File name extension for the file system object, not including the dot (.) that separates the extension from the file name.</span></span>

<span data-ttu-id="13760-285">Exemples : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="13760-285">Examples: "txt", "mof", "mdb"</span></span>

<span data-ttu-id="13760-286">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-286">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-287">**FileName**</span><span class="sxs-lookup"><span data-stu-id="13760-287">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-290">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="13760-290">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-291">Nom de fichier (sans le point ou l’extension) du fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-291">File name (without the dot or extension) of the file.</span></span>

<span data-ttu-id="13760-292">Exemple : « Autoexec »</span><span class="sxs-lookup"><span data-stu-id="13760-292">Example: "autoexec"</span></span>

<span data-ttu-id="13760-293">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-293">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-294">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="13760-294">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-295">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13760-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13760-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-297">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="13760-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="13760-298">Taille de l’objet système de fichiers, en octets.</span><span class="sxs-lookup"><span data-stu-id="13760-298">Size of the file system object, in bytes.</span></span> <span data-ttu-id="13760-299">Bien que les dossiers possèdent une propriété **FileSize** , la valeur 0 est toujours retournée.</span><span class="sxs-lookup"><span data-stu-id="13760-299">Although folders possess a **FileSize** property, the value 0 is always returned.</span></span> <span data-ttu-id="13760-300">Pour déterminer la taille d’un dossier, utilisez FileSystemObject ou ajoutez la taille de tous les fichiers stockés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-300">To determine the size of a folder, use the FileSystemObject or add up the size of all the files stored in the folder.</span></span>

<span data-ttu-id="13760-301">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="13760-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="13760-302">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-303">**FileType**</span><span class="sxs-lookup"><span data-stu-id="13760-303">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-306">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="13760-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="13760-307">Type de fichier (indiqué par la propriété d' **extension** ).</span><span class="sxs-lookup"><span data-stu-id="13760-307">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="13760-308">Par exemple, un fichier. mdb est susceptible d’avoir le type de fichier application Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="13760-308">For example, an .mdb file is likely to have the file type Microsoft Access Application.</span></span> <span data-ttu-id="13760-309">Un fichier. asp a probablement le type de fichier document HTML.</span><span class="sxs-lookup"><span data-stu-id="13760-309">An .asp file likely has the file type HTML Document.</span></span> <span data-ttu-id="13760-310">Les dossiers sont généralement signalés simplement comme dossiers.</span><span class="sxs-lookup"><span data-stu-id="13760-310">Folders are typically reported simply as Folder.</span></span>

<span data-ttu-id="13760-311">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-311">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-312">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13760-312">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-315">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="13760-315">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-316">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-316">Class of the file system.</span></span>

<span data-ttu-id="13760-317">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-317">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-318">**FSName**</span><span class="sxs-lookup"><span data-stu-id="13760-318">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-321">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="13760-321">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="13760-322">Type de système de fichiers (NTFS, FAT, FAT32) installé sur le lecteur où se trouve le fichier ou le dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-322">Type of file system (NTFS, FAT, FAT32) installed on the drive where the file or folder is located.</span></span>

<span data-ttu-id="13760-323">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-324">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="13760-324">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-325">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-327">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="13760-327">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="13760-328">Indique si l’objet de système de fichiers est masqué.</span><span class="sxs-lookup"><span data-stu-id="13760-328">Indicates whether the file system object is hidden.</span></span> <span data-ttu-id="13760-329">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="13760-329">If **True**, the file is hidden.</span></span>

<span data-ttu-id="13760-330">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-331">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13760-331">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-332">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13760-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13760-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-334">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="13760-334">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="13760-335">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="13760-335">Indicates when the object was installed.</span></span> <span data-ttu-id="13760-336">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="13760-336">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="13760-337">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13760-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-338">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="13760-338">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-339">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13760-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13760-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-341">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="13760-341">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="13760-342">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-342">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="13760-343">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-343">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="13760-344">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="13760-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="13760-345">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="13760-345">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-346">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13760-346">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13760-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-348">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="13760-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="13760-349">Date du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-349">Date the file was last accessed.</span></span> <span data-ttu-id="13760-350">Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="13760-350">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="13760-351">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-351">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-352">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="13760-352">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-353">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13760-353">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13760-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-355">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="13760-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="13760-356">Date de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-356">Date the file was last modified.</span></span> <span data-ttu-id="13760-357">Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span><span class="sxs-lookup"><span data-stu-id="13760-357">For more information on working with WMI date and time formats, see [WMI Tasks: Dates and Times](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).</span></span>

<span data-ttu-id="13760-358">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-358">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-359">**Nom**</span><span class="sxs-lookup"><span data-stu-id="13760-359">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-362">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13760-362">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13760-363">La propriété Name est une chaîne représentant le nom hérité qui sert de clé à une instance de fichier logique dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-363">The Name property is a string representing the inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="13760-364">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="13760-364">Full path names should be provided.</span></span> <span data-ttu-id="13760-365">Exemple : C : \\ \\ système Windows \\win.ini</span><span class="sxs-lookup"><span data-stu-id="13760-365">Example: C:\\Windows\\system\\win.ini</span></span>

<span data-ttu-id="13760-366">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-366">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-367">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="13760-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-370">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="13760-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="13760-371">Chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="13760-371">Path for the file.</span></span> <span data-ttu-id="13760-372">Le chemin d’accès comprend les barres obliques inverses de début et de fin, mais pas la lettre de lecteur ou le nom de dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-372">The path includes the leading and trailing backslashes, but not the drive letter or the folder name.</span></span>

<span data-ttu-id="13760-373">Pour le dossier c : \\ Windows \\ system32 \\ WBEM, le chemin d’accès est \\ Windows \\ system32 \\ .</span><span class="sxs-lookup"><span data-stu-id="13760-373">For the folder c:\\windows\\system32\\wbem, the path is \\windows\\system32\\.</span></span> <span data-ttu-id="13760-374">Pour le dossier c : \\ scripts, le chemin d’accès est \\ .</span><span class="sxs-lookup"><span data-stu-id="13760-374">For the folder c:\\scripts, the path is \\.</span></span>

<span data-ttu-id="13760-375">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-375">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-376">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="13760-376">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-377">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-379">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="13760-379">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="13760-380">Indique si vous pouvez lire des éléments dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-380">Indicates whether you can read items in the folder.</span></span> <span data-ttu-id="13760-381">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="13760-381">If **True**, the file can be read.</span></span>

<span data-ttu-id="13760-382">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-382">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-383">**État**</span><span class="sxs-lookup"><span data-stu-id="13760-383">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-384">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13760-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13760-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-386">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="13760-386">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="13760-387">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13760-387">String that indicates the current status of the object.</span></span>

<span data-ttu-id="13760-388">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13760-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13760-389">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="13760-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="13760-390">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="13760-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="13760-391">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="13760-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13760-392">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="13760-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13760-393">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="13760-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="13760-394">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="13760-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="13760-395">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="13760-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="13760-396">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="13760-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13760-397">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="13760-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="13760-398">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="13760-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="13760-399">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="13760-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="13760-400">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="13760-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="13760-401">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="13760-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13760-402">**Système**</span><span class="sxs-lookup"><span data-stu-id="13760-402">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-403">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-403">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-405">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="13760-405">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="13760-406">Indique si l’objet est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="13760-406">Indicates whether the object is a system file.</span></span> <span data-ttu-id="13760-407">Si la **valeur est true**, le fichier est un fichier système</span><span class="sxs-lookup"><span data-stu-id="13760-407">If **True**, the file is a system file</span></span>

<span data-ttu-id="13760-408">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-408">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="13760-409">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="13760-409">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13760-410">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13760-410">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13760-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13760-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13760-412">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="13760-412">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="13760-413">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="13760-413">If **True**, the file can be written.</span></span>

<span data-ttu-id="13760-414">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="13760-414">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13760-415">Notes</span><span class="sxs-lookup"><span data-stu-id="13760-415">Remarks</span></span>

<span data-ttu-id="13760-416">La classe de **\_ répertoire win32** est dérivée du [**\_ répertoire CIM**](cim-directory.md).</span><span class="sxs-lookup"><span data-stu-id="13760-416">The **Win32\_Directory** class is derived from [**CIM\_Directory**](cim-directory.md).</span></span>

<span data-ttu-id="13760-417">**Vue d’ensemble**</span><span class="sxs-lookup"><span data-stu-id="13760-417">**Overview**</span></span>

<span data-ttu-id="13760-418">Les dossiers sont des objets de système de fichiers conçus pour contenir d’autres objets de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-418">Folders are file system objects designed to contain other file system objects.</span></span> <span data-ttu-id="13760-419">Toutefois, cela ne signifie pas que tous les dossiers sont similaires.</span><span class="sxs-lookup"><span data-stu-id="13760-419">This does not mean that all folders are alike, however.</span></span> <span data-ttu-id="13760-420">Au lieu de cela, les dossiers peuvent varier considérablement.</span><span class="sxs-lookup"><span data-stu-id="13760-420">Instead, folders can vary considerably.</span></span> <span data-ttu-id="13760-421">Certains dossiers sont des dossiers du système d’exploitation, qui ne doivent généralement pas être modifiés par un script.</span><span class="sxs-lookup"><span data-stu-id="13760-421">Some folders are operating system folders, which generally should not be modified by a script.</span></span> <span data-ttu-id="13760-422">Certains dossiers sont en lecture seule, ce qui signifie que les utilisateurs peuvent accéder au contenu de ce dossier, mais qu’ils ne peuvent pas ajouter, supprimer ou modifier ces contenus.</span><span class="sxs-lookup"><span data-stu-id="13760-422">Some folders are read-only, which means that users can access the contents of that folder but cannot add to, delete from, or modify those contents.</span></span> <span data-ttu-id="13760-423">Certains dossiers sont compressés pour un stockage optimal, tandis que d’autres sont masqués et invisibles pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="13760-423">Some folders are compressed for optimal storage, while others are hidden and not visible to users.</span></span>

<span data-ttu-id="13760-424">WMI utilise la classe de **\_ répertoire win32** pour gérer les dossiers.</span><span class="sxs-lookup"><span data-stu-id="13760-424">WMI uses the **Win32\_Directory** class to manage folders.</span></span> <span data-ttu-id="13760-425">De manière significative, les propriétés et les méthodes disponibles dans cette classe sont identiques aux propriétés et aux méthodes disponibles dans la classe de [**\_ fichier de fichier CIM**](cim-datafile.md) , la classe utilisée pour gérer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-425">Significantly, the properties and methods available in this class are identical to the properties and methods available in the [**CIM\_DataFile**](cim-datafile.md) class, the class used to manage files.</span></span> <span data-ttu-id="13760-426">Cela signifie qu’une fois que vous avez appris à gérer des dossiers à l’aide de WMI, vous pouvez, sans aucun travail supplémentaire, savoir comment gérer les fichiers.</span><span class="sxs-lookup"><span data-stu-id="13760-426">This means that after you have learned how to manage folders using WMI, you will, without any extra work, also know how to manage files.</span></span>

<span data-ttu-id="13760-427">La classe d’association de [**\_ sous-répertoire win32**](win32-subdirectory.md) est également utilisée pour gérer des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="13760-427">The [**Win32\_Subdirectory**](win32-subdirectory.md) association class is also used to manage files and folders.</span></span> <span data-ttu-id="13760-428">La classe de **\_ sous-répertoire win32** lie un dossier et ses sous-dossiers immédiats.</span><span class="sxs-lookup"><span data-stu-id="13760-428">The **Win32\_Subdirectory** class relates a folder and its immediate subfolders.</span></span> <span data-ttu-id="13760-429">Par exemple, dans la structure de dossiers C : \\ scripts \\ journaux, logs est un sous-dossier de scripts et scripts est un sous-dossier du dossier racine C : \\ .</span><span class="sxs-lookup"><span data-stu-id="13760-429">For example, in the folder structure C:\\Scripts\\Logs, Logs is a subfolder of Scripts, and Scripts is a subfolder of the root folder C:\\.</span></span> <span data-ttu-id="13760-430">Toutefois, les journaux ne sont pas considérés comme un sous-dossier de C : \\ .</span><span class="sxs-lookup"><span data-stu-id="13760-430">However, Logs is not considered a subfolder of C:\\.</span></span>

<span data-ttu-id="13760-431">Vous pouvez récupérer les propriétés de n’importe quel dossier dans le système de fichiers à l’aide de la classe de **\_ répertoire win32** .</span><span class="sxs-lookup"><span data-stu-id="13760-431">You can retrieve the properties of any folder in the file system using the **Win32\_Directory** class.</span></span> <span data-ttu-id="13760-432">Les propriétés disponibles à l’aide de cette classe sont indiquées dans le tableau 11,1.</span><span class="sxs-lookup"><span data-stu-id="13760-432">The properties available using this class are shown in Table 11.1.</span></span> <span data-ttu-id="13760-433">Pour récupérer les propriétés d’un seul dossier, construisez une requête WQL (Windows Query Language) pour la classe de **\_ répertoire win32** , en veillant à inclure le nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="13760-433">To retrieve the properties for a single folder, construct a Windows Query Language (WQL) query for the **Win32\_Directory** class, making sure that you include the name of the folder.</span></span> <span data-ttu-id="13760-434">Par exemple, cette requête est liée au dossier D : \\ Archive :</span><span class="sxs-lookup"><span data-stu-id="13760-434">For example, this query binds to the folder D:\\Archive:</span></span>

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

<span data-ttu-id="13760-435">Lorsque vous spécifiez un nom de fichier ou de dossier dans une requête WQL, veillez à utiliser deux barres obliques \\ \\ inverses () pour séparer les composants du chemin.</span><span class="sxs-lookup"><span data-stu-id="13760-435">When specifying a file or folder name in a WQL query, be sure you use two backslashes (\\\\) to separate path components.</span></span>

<span data-ttu-id="13760-436">Si vous souhaitez limiter la récupération des données à un seul lecteur de disque, incluez une clause WHERE spécifiant la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="13760-436">If you want to limit data retrieval to a single disk drive, include a Where clause specifying the drive letter.</span></span> <span data-ttu-id="13760-437">Par exemple, cette requête renvoie une liste de tous les dossiers sur le lecteur C :</span><span class="sxs-lookup"><span data-stu-id="13760-437">For example, this query returns a list of all the folders on drive C:</span></span>

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

<span data-ttu-id="13760-438">Si vous devez énumérer tous les dossiers d’un ordinateur, sachez que cette requête peut prendre plus de temps.</span><span class="sxs-lookup"><span data-stu-id="13760-438">If you need to enumerate all the folders on a computer, be aware that this query can take an extended time to complete.</span></span>

## <a name="examples"></a><span data-ttu-id="13760-439">Exemples</span><span class="sxs-lookup"><span data-stu-id="13760-439">Examples</span></span>

<span data-ttu-id="13760-440">L’exemple VBScript suivant récupère les propriétés du dossier C : \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="13760-440">The following VBScript sample retrieves properties for the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



<span data-ttu-id="13760-441">L’exemple VBScript suivant retourne une liste de tous les dossiers masqués sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="13760-441">The following VBScript sample returns a list of all the hidden folders on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="13760-442">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13760-442">Requirements</span></span>



| <span data-ttu-id="13760-443">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13760-443">Requirement</span></span> | <span data-ttu-id="13760-444">Valeur</span><span class="sxs-lookup"><span data-stu-id="13760-444">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13760-445">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13760-445">Minimum supported client</span></span><br/> | <span data-ttu-id="13760-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13760-446">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13760-447">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13760-447">Minimum supported server</span></span><br/> | <span data-ttu-id="13760-448">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13760-448">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13760-449">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13760-449">Namespace</span></span><br/>                | <span data-ttu-id="13760-450">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="13760-450">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13760-451">MOF</span><span class="sxs-lookup"><span data-stu-id="13760-451">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13760-452"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13760-452"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13760-453">DLL</span><span class="sxs-lookup"><span data-stu-id="13760-453">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13760-454"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13760-454"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13760-455">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13760-455">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13760-456">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="13760-456">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dt>

<span data-ttu-id="13760-457">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13760-457">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

