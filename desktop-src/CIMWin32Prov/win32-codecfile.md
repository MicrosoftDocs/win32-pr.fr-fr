---
description: Le \_ CodecFile Win32&\# 32 ; La classe WMI représente le codec audio ou vidéo installé sur le système informatique.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111234"
---
# <a name="win32_codecfile-class"></a><span data-ttu-id="b5fa0-103">\_Classe CodecFile Win32</span><span class="sxs-lookup"><span data-stu-id="b5fa0-103">Win32\_CodecFile class</span></span>

<span data-ttu-id="b5fa0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CodecFile** WMI représente le codec audio ou vidéo installé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-104">The **Win32\_CodecFile** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the audio or video codec installed on the computer system.</span></span> <span data-ttu-id="b5fa0-105">Les codecs convertissent un type de format de média vers un autre, en général un format compressé dans un format non compressé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-105">Codecs convert one media format type to another, typically a compressed format to an uncompressed format.</span></span> <span data-ttu-id="b5fa0-106">Le nom « codec » est dérivé d’une combinaison de compresser et décompresser.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-106">The name "codec" is derived from a combination of compress and decompress.</span></span> <span data-ttu-id="b5fa0-107">Par exemple, un codec peut convertir un format compressé, tel que MS-ADPCM, en un format non compressé, tel que PCM, que le matériel audio peut lire directement.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-107">For example, a codec can convert a compressed format, such as MS-ADPCM, to an uncompressed format such as PCM, which most audio hardware can play directly.</span></span>

<span data-ttu-id="b5fa0-108">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b5fa0-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5fa0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5fa0-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
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
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="b5fa0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b5fa0-111">Members</span></span>

<span data-ttu-id="b5fa0-112">La classe **Win32 \_ CodecFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5fa0-112">The **Win32\_CodecFile** class has these types of members:</span></span>

-   [<span data-ttu-id="b5fa0-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5fa0-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b5fa0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5fa0-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b5fa0-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b5fa0-115">Methods</span></span>

<span data-ttu-id="b5fa0-116">La classe **Win32 \_ CodecFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-116">The **Win32\_CodecFile** class has these methods.</span></span>



| <span data-ttu-id="b5fa0-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="b5fa0-117">Method</span></span>                                                                                             | <span data-ttu-id="b5fa0-118">Description</span><span class="sxs-lookup"><span data-stu-id="b5fa0-118">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5fa0-119">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-119">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-win32-codecfile.md)     | <span data-ttu-id="b5fa0-120">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-120">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="b5fa0-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | <span data-ttu-id="b5fa0-122">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-122">Changes the security permissions for the logical file specified in the object path.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="b5fa0-123">**Dens**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-123">**Compress**</span></span>](compress-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="b5fa0-124">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-124">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="b5fa0-125">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-125">**CompressEx**</span></span>](compressex-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="b5fa0-126">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-126">Compresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="b5fa0-127">**Copier**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-127">**Copy**</span></span>](copy-method-in-class-win32-codecfile.md)                                               | <span data-ttu-id="b5fa0-128">Copie le fichier ou le répertoire logique spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-128">Copies the logical file or directory specified in the object path to the location specified by the input parameter.</span></span><br/>                                                                                         |
| [<span data-ttu-id="b5fa0-129">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-129">**CopyEx**</span></span>](copyex-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="b5fa0-130">Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-130">Class method that copies the logical file or directory specified in the object path to the location specified by the FileName parameter.</span></span><br/>                                                                    |
| [<span data-ttu-id="b5fa0-131">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-131">**Delete**</span></span>](delete-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="b5fa0-132">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-132">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="b5fa0-133">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-133">**DeleteEx**</span></span>](deleteex-method-in-class-win32-codecfile.md)                                       | <span data-ttu-id="b5fa0-134">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-134">Deletes the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="b5fa0-135">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-135">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-win32-codecfile.md)           | <span data-ttu-id="b5fa0-136">Détermine si l’appelant a les autorisations agrégées spécifiées par l’argument d' **autorisation** non seulement sur l’objet de fichier, mais sur le partage sur lequel le fichier ou le répertoire réside (s’il se trouve sur un partage).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-136">Determines whether the caller has the aggregated permissions specified by the **permission** argument not only on the file object, but on the share the file or directory resides on (if it is on a share).</span></span><br/> |
| [<span data-ttu-id="b5fa0-137">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-137">**Rename**</span></span>](rename-method-in-class-win32-codecfile.md)                                           | <span data-ttu-id="b5fa0-138">Méthode de classe qui renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-138">Class method that renames the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="b5fa0-139">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-139">**TakeOwnerShip**</span></span>](takeownership-method-in-class-win32-codecfile.md)                             | <span data-ttu-id="b5fa0-140">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-140">Obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="b5fa0-141">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-141">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-win32-codecfile.md)                         | <span data-ttu-id="b5fa0-142">Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-142">Class method that obtains ownership of the logical file specified in the object path.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="b5fa0-143">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-143">**Uncompress**</span></span>](uncompress-method-in-class-win32-codecfile.md)                                   | <span data-ttu-id="b5fa0-144">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-144">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="b5fa0-145">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-145">**UncompressEx**</span></span>](uncompressex-method-in-class-win32-codecfile.md)                               | <span data-ttu-id="b5fa0-146">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-146">Uncompresses the logical file (or directory) specified in the object path.</span></span><br/>                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="b5fa0-147">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5fa0-147">Properties</span></span>

<span data-ttu-id="b5fa0-148">La classe **Win32 \_ CodecFile** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-148">The **Win32\_CodecFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5fa0-149">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-149">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-152">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-152">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-153">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur le fichier de codec.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-153">Bitmask that represents the access rights required to access or perform specific operations on the codec file.</span></span> <span data-ttu-id="b5fa0-154">Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-154">For bit values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="b5fa0-155">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-155">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="b5fa0-156">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-156">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="b5fa0-157">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-157">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="b5fa0-158">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-158">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="b5fa0-159">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-159">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="b5fa0-160">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-160">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="b5fa0-161">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-161">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="b5fa0-162">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-162">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="b5fa0-163">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-163">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="b5fa0-164">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-164">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="b5fa0-165">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-165">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="b5fa0-166">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-166">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="b5fa0-167">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-167">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="b5fa0-168">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-168">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="b5fa0-169">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-169">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="b5fa0-170">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-170">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5fa0-171">**Archive**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-171">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-174">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-175">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-175">If **True**, the file should be archived.</span></span>

<span data-ttu-id="b5fa0-176">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-176">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-177">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-177">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-180">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-181">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-181">Short description of the object.</span></span>

<span data-ttu-id="b5fa0-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-183">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-183">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-186">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-187">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-187">If **True**, the file is compressed.</span></span>

<span data-ttu-id="b5fa0-188">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-188">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-189">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-189">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-192">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-192">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-193">Algorithme ou outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-193">Algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b5fa0-194">Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez les mots suivants : « inconnu » pour indiquer qu’il n’est pas connu que le fichier logique est compressé ou non ; « Compressed » pour représenter le fait que le fichier est compressé, mais que son schéma de compression n’est pas connu ou n’est pas divulgué ; et « non compressés » pour indiquer que le fichier logique n’est pas compressé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-194">If it is not possible (or not desired) to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the logical file is compressed or not; "Compressed" to represent that the file is compressed but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the logical file is not compressed.</span></span>

<span data-ttu-id="b5fa0-195">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-195">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-199">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-199">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-200">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-200">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b5fa0-201">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-201">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b5fa0-202">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-202">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-203">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-203">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-204">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-204">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-206">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-206">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-207">Date de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-207">File creation date.</span></span>

<span data-ttu-id="b5fa0-208">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-209">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-209">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-212">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-213">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-213">Class of the computer system.</span></span>

<span data-ttu-id="b5fa0-214">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-214">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-215">**CSName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-215">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-218">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-218">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-219">Chaîne représentant le nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-219">String representing the name of the computer system.</span></span>

<span data-ttu-id="b5fa0-220">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-221">**Description**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-221">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-224">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ MediaResources \\ \\ ICM \| Description")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-224">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\icm\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-225">Nom complet du pilote du codec.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-225">Full name of the codec driver.</span></span> <span data-ttu-id="b5fa0-226">Cette chaîne est destinée à être affichée dans des espaces de grande taille (descriptifs).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-226">This string is intended to be displayed in large (descriptive) spaces.</span></span>

<span data-ttu-id="b5fa0-227">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b5fa0-228">Exemple : « convertisseur Microsoft PCM »</span><span class="sxs-lookup"><span data-stu-id="b5fa0-228">Example: "Microsoft PCM Converter"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-229">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-229">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-232">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-232">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-233">Lettre de lecteur (y compris le signe deux-points) du fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-233">Drive letter (including colon) of the file.</span></span>

<span data-ttu-id="b5fa0-234">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-235">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="b5fa0-235">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-236">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-236">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-239">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-240">Nom de fichier compatible DOS pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-240">DOS-compatible file name for this file.</span></span>

<span data-ttu-id="b5fa0-241">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-242">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="b5fa0-242">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-243">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-243">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-244">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-246">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-247">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-247">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="b5fa0-248">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-248">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-249">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-249">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-252">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-252">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-253">Algorithme ou outil utilisé pour chiffrer le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-253">Algorithm or tool used to encrypt the logical file.</span></span> <span data-ttu-id="b5fa0-254">Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de chiffrement (pour des raisons de sécurité, par exemple), utilisez les mots suivants : « inconnu » pour indiquer qu’il est impossible de savoir si le fichier logique est chiffré ou non ; « Chiffré » pour représenter le chiffrement du fichier, mais son schéma de chiffrement n’est pas connu ou n’est pas divulgué ; et « non chiffrés » pour représenter le fait que le fichier logique n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-254">If it is not possible (or not desired) to describe the encryption scheme (perhaps for security reasons), use the following words: "Unknown" to represent that it is not known whether the logical file is encrypted or not; "Encrypted" to represent that the file is encrypted but either its encryption scheme is not known or not disclosed; and "Not Encrypted" to represent that the logical file is not encrypted.</span></span>

<span data-ttu-id="b5fa0-255">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-255">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-256">**Extension**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-256">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-259">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-259">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-260">Extension de nom de fichier (sans point).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-260">File name extension (without the dot).</span></span>

<span data-ttu-id="b5fa0-261">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-261">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-262">Exemples : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="b5fa0-262">Examples: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-263">**FileName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-263">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-266">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-266">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-267">Nom (sans l’extension) du fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-267">Name (without the extension) of the file.</span></span>

<span data-ttu-id="b5fa0-268">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-268">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-269">Exemple : « Autoexec »</span><span class="sxs-lookup"><span data-stu-id="b5fa0-269">Example: "autoexec"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-270">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-270">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-271">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-273">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-274">Taille du fichier (en octets).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-274">Size of the file (in bytes).</span></span>

<span data-ttu-id="b5fa0-275">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-276">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-276">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-277">**FileType**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-277">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-280">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-281">Type de fichier (indiqué par la propriété d' **extension** ).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-281">File type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="b5fa0-282">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-283">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-283">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-286">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-286">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-287">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-287">Class of the file system.</span></span>

<span data-ttu-id="b5fa0-288">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-289">**FSName**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-289">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-292">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-292">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-293">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-293">Name of the file system.</span></span>

<span data-ttu-id="b5fa0-294">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-295">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-295">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-298">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ drivers. desc")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-298">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\drivers.desc")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-299">Codec représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-299">Codec represented by this class.</span></span>

<span data-ttu-id="b5fa0-300">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="b5fa0-300">The values are:</span></span>

<dl> <dd><span data-ttu-id="b5fa0-301">HD</span><span class="sxs-lookup"><span data-stu-id="b5fa0-301">"Audio"</span></span></dd> <dd><span data-ttu-id="b5fa0-302">Vidéosurveillance</span><span class="sxs-lookup"><span data-stu-id="b5fa0-302">"Video"</span></span></dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

<span data-ttu-id="b5fa0-303">**Audio** (« audio »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-303">**Audio** ("Audio")</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="b5fa0-304">**Vidéo** (« vidéo »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-304">**Video** ("Video")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5fa0-305">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-305">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-306">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-306">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-308">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-308">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-309">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-309">If **True**, the file is hidden.</span></span>

<span data-ttu-id="b5fa0-310">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-310">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-312">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-314">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-315">L’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-315">Object was installed.</span></span> <span data-ttu-id="b5fa0-316">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-316">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b5fa0-317">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-318">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-318">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-319">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-321">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-321">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-322">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-322">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="b5fa0-323">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-323">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-324">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-324">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-325">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-325">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-326">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-328">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-329">Le fichier a été accédé pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-329">File was last accessed.</span></span>

<span data-ttu-id="b5fa0-330">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-330">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-331">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-331">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-332">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-334">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-335">Le fichier a été modifié pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-335">File was last modified.</span></span>

<span data-ttu-id="b5fa0-336">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-336">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-337">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-337">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-340">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-340">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-341">Chaîne du fabricant de la ressource de version, si celle-ci est présente.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-341">Manufacturer string from version resource, if one is present.</span></span>

<span data-ttu-id="b5fa0-342">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-342">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-343">**Nom**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-343">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-346">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-347">Nom hérité qui sert de clé d’une instance de fichier logique dans un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-347">Inherited name that serves as a key of a logical file instance within a file system.</span></span> <span data-ttu-id="b5fa0-348">Les noms de chemin d’accès complets doivent être fournis.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-348">Full path names should be provided.</span></span>

<span data-ttu-id="b5fa0-349">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b5fa0-350">Exemple : « C : \\ \\ système Windows \\win.ini »</span><span class="sxs-lookup"><span data-stu-id="b5fa0-350">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-351">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-351">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-354">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-354">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-355">Chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-355">Path of the file.</span></span> <span data-ttu-id="b5fa0-356">Cela comprend les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-356">This includes leading and trailing backslashes.</span></span>

<span data-ttu-id="b5fa0-357">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-357">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="b5fa0-358">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="b5fa0-358">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-359">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-359">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-360">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-362">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-363">Le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-363">File can be read.</span></span>

<span data-ttu-id="b5fa0-364">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-364">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-365">**État**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-368">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-369">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-369">Current status of the object.</span></span> <span data-ttu-id="b5fa0-370">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b5fa0-371">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b5fa0-372">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="b5fa0-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b5fa0-373">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b5fa0-374">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b5fa0-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b5fa0-376">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b5fa0-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b5fa0-377">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b5fa0-378">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b5fa0-379">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b5fa0-380">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b5fa0-381">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b5fa0-382">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b5fa0-383">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b5fa0-384">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b5fa0-385">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b5fa0-386">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b5fa0-387">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b5fa0-388">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b5fa0-389">**Système**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-389">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-390">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-392">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-392">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-393">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-393">If **True**, the file is a system file.</span></span>

<span data-ttu-id="b5fa0-394">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-394">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-395">**Version**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-395">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-396">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-398">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("version")</span><span class="sxs-lookup"><span data-stu-id="b5fa0-398">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-399">Chaîne de version de la ressource de version, si celle-ci est présente.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-399">Version string from version resource, if one is present.</span></span>

<span data-ttu-id="b5fa0-400">Cette propriété est héritée [**du \_ fichier de fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-400">This property is inherited from [**CIM\_DataFile**](cim-datafile.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fa0-401">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-401">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5fa0-402">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5fa0-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5fa0-404">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="b5fa0-404">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="b5fa0-405">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="b5fa0-405">If **True**, the file can be written.</span></span>

<span data-ttu-id="b5fa0-406">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-406">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5fa0-407">Notes</span><span class="sxs-lookup"><span data-stu-id="b5fa0-407">Remarks</span></span>

<span data-ttu-id="b5fa0-408">La classe **Win32 \_ CodecFile** est dérivée du [**fichier de \_ fichier CIM**](cim-datafile.md).</span><span class="sxs-lookup"><span data-stu-id="b5fa0-408">The **Win32\_CodecFile** class is derived from [**CIM\_DataFile**](cim-datafile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5fa0-409">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5fa0-409">Requirements</span></span>



| <span data-ttu-id="b5fa0-410">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5fa0-410">Requirement</span></span> | <span data-ttu-id="b5fa0-411">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5fa0-411">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fa0-412">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5fa0-412">Minimum supported client</span></span><br/> | <span data-ttu-id="b5fa0-413">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5fa0-413">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5fa0-414">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5fa0-414">Minimum supported server</span></span><br/> | <span data-ttu-id="b5fa0-415">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5fa0-415">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5fa0-416">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5fa0-416">Namespace</span></span><br/>                | <span data-ttu-id="b5fa0-417">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b5fa0-417">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5fa0-418">MOF</span><span class="sxs-lookup"><span data-stu-id="b5fa0-418">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5fa0-419"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5fa0-419"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5fa0-420">DLL</span><span class="sxs-lookup"><span data-stu-id="b5fa0-420">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5fa0-421"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5fa0-421"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5fa0-422">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5fa0-422">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5fa0-423">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="b5fa0-423">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

<span data-ttu-id="b5fa0-424">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5fa0-424">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

