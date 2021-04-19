---
description: La \_ classe de répertoire CIM représente un type de fichier qui regroupe logiquement les fichiers de données qu’elle contient et fournit des informations de chemin d’accès pour les fichiers groupés.
ms.assetid: a9594f53-08f0-4a47-9edc-51686c80c5ea
ms.tgt_platform: multiple
title: Classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory
- CIM_Directory.AccessMask
- CIM_Directory.Archive
- CIM_Directory.Caption
- CIM_Directory.Compressed
- CIM_Directory.CompressionMethod
- CIM_Directory.CreationClassName
- CIM_Directory.CreationDate
- CIM_Directory.CSCreationClassName
- CIM_Directory.CSName
- CIM_Directory.Description
- CIM_Directory.Drive
- CIM_Directory.EightDotThreeFileName
- CIM_Directory.Encrypted
- CIM_Directory.EncryptionMethod
- CIM_Directory.Extension
- CIM_Directory.FileName
- CIM_Directory.FileSize
- CIM_Directory.FileType
- CIM_Directory.FSCreationClassName
- CIM_Directory.FSName
- CIM_Directory.Hidden
- CIM_Directory.InstallDate
- CIM_Directory.InUseCount
- CIM_Directory.LastAccessed
- CIM_Directory.LastModified
- CIM_Directory.Name
- CIM_Directory.Path
- CIM_Directory.Readable
- CIM_Directory.Status
- CIM_Directory.System
- CIM_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cebab65cc067018b3a57aa5f6890fffad1cb4c7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517196"
---
# <a name="cim_directory-class"></a><span data-ttu-id="8d0d8-103">\_Classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="8d0d8-103">CIM\_Directory class</span></span>

<span data-ttu-id="8d0d8-104">La classe de **\_ répertoire CIM** représente un type de fichier qui regroupe logiquement les fichiers de données qu’elle contient et fournit des informations de chemin d’accès pour les fichiers groupés.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-104">The **CIM\_Directory** class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d0d8-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d0d8-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d0d8-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8d0d8-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d0d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d0d8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C55F-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Directories (CIM)"), AMENDMENT]
class CIM_Directory : CIM_LogicalFile
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
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  boolean  Writeable;
};
```

## <a name="members"></a><span data-ttu-id="8d0d8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8d0d8-110">Members</span></span>

<span data-ttu-id="8d0d8-111">La classe de **\_ répertoire CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8d0d8-111">The **CIM\_Directory** class has these types of members:</span></span>

-   [<span data-ttu-id="8d0d8-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d0d8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8d0d8-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d0d8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8d0d8-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d0d8-114">Methods</span></span>

<span data-ttu-id="8d0d8-115">La classe de **\_ répertoire CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-115">The **CIM\_Directory** class has these methods.</span></span>



| <span data-ttu-id="8d0d8-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d0d8-116">Method</span></span>                                                                                           | <span data-ttu-id="8d0d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="8d0d8-117">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d0d8-118">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-118">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)     | <span data-ttu-id="8d0d8-119">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-119">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="8d0d8-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-120">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="8d0d8-121">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-121">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md) | <span data-ttu-id="8d0d8-122">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-122">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="8d0d8-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-123">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="8d0d8-124">**Dens**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-124">**Compress**</span></span>](compress-method-in-class-cim-directory.md)                                       | <span data-ttu-id="8d0d8-125">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-125">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-126">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="8d0d8-127">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-127">**CompressEx**</span></span>](compressex-method-in-class-cim-directory.md)                                   | <span data-ttu-id="8d0d8-128">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-128">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-129">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-129">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="8d0d8-130">**Copier**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-130">**Copy**</span></span>](copy-method-in-class-cim-directory.md)                                               | <span data-ttu-id="8d0d8-131">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-131">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="8d0d8-132">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-132">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="8d0d8-133">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-133">**CopyEx**</span></span>](copyex-method-in-class-cim-directory.md)                                           | <span data-ttu-id="8d0d8-134">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-134">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="8d0d8-135">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-135">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="8d0d8-136">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-136">**Delete**</span></span>](delete-method-in-class-cim-directory.md)                                           | <span data-ttu-id="8d0d8-137">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-137">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-138">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-138">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="8d0d8-139">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-139">**DeleteEx**</span></span>](deleteex-method-in-class-cim-directory.md)                                       | <span data-ttu-id="8d0d8-140">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-140">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-141">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-141">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="8d0d8-142">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-142">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)           | <span data-ttu-id="8d0d8-143">Détermine si l’appelant dispose des autorisations agrégées spécifiées par l’argument d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="8d0d8-143">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="8d0d8-144">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-144">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="8d0d8-145">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-145">**Rename**</span></span>](rename-method-in-class-cim-directory.md)                                           | <span data-ttu-id="8d0d8-146">Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-146">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-147">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-147">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="8d0d8-148">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-148">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-directory.md)                             | <span data-ttu-id="8d0d8-149">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-149">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="8d0d8-150">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-150">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="8d0d8-151">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-151">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-directory.md)                         | <span data-ttu-id="8d0d8-152">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-152">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="8d0d8-153">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-153">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="8d0d8-154">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-154">**Uncompress**</span></span>](uncompress-method-in-class-cim-directory.md)                                   | <span data-ttu-id="8d0d8-155">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-155">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-156">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-156">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="8d0d8-157">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-157">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-directory.md)                               | <span data-ttu-id="8d0d8-158">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-158">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8d0d8-159">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-159">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="8d0d8-160">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d0d8-160">Properties</span></span>

<span data-ttu-id="8d0d8-161">La classe de **\_ répertoire CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-161">The **CIM\_Directory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d0d8-162">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-162">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-165">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-165">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-166">Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-166">Bitmask that represents the access rights required to access or perform specific operations on the directory.</span></span> <span data-ttu-id="8d0d8-167">Pour obtenir les valeurs, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-167">For values, see [**File and Directory Access Rights Constants**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).</span></span>

> [!Note]  
> <span data-ttu-id="8d0d8-168">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-168">On FAT volumes, the **FULL\_ACCESS** value is returned instead, which indicates no security has been set on the object.</span></span>

 

<span data-ttu-id="8d0d8-169">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-169">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="8d0d8-170">**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-170">**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="8d0d8-171">**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-171">**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="8d0d8-172">**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-172">**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="8d0d8-173">**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-173">**FILE\_READ\_EA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="8d0d8-174">**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-174">**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="8d0d8-175">**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-175">**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="8d0d8-176">**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-176">**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="8d0d8-177">**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-177">**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="8d0d8-178">**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-178">**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="8d0d8-179">**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-179">**DELETE** (65536)</span></span>


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="8d0d8-180">**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-180">**READ\_CONTROL** (131072)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="8d0d8-181">**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-181">**WRITE\_DAC** (262144)</span></span>


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="8d0d8-182">**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-182">**WRITE\_OWNER** (524288)</span></span>


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="8d0d8-183">**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-183">**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d0d8-184">**Archive**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-184">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-185">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-187">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-188">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-188">If **True**, the file should be archived.</span></span>

<span data-ttu-id="8d0d8-189">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-189">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-193">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-194">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-194">Short textual description of the object.</span></span>

<span data-ttu-id="8d0d8-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-196">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-196">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-197">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-199">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-199">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-200">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-200">If **True**, the file is compressed.</span></span>

<span data-ttu-id="8d0d8-201">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-201">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-202">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-202">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-205">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-205">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-206">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-206">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="8d0d8-207">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-207">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="8d0d8-208">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-208">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="8d0d8-209">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-209">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="8d0d8-210">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-210">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-211">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-211">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-214">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-214">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-215">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-215">Name of the class.</span></span>

<span data-ttu-id="8d0d8-216">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-216">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-217">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-217">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-218">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-220">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-220">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-221">Date et heure de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-221">Date and time that the file was created.</span></span>

<span data-ttu-id="8d0d8-222">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-222">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-223">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-223">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-226">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-226">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-227">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-227">Class of the computer system.</span></span>

<span data-ttu-id="8d0d8-228">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-228">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-229">**CSName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-229">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-232">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-232">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-233">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-233">Name of the computer system.</span></span>

<span data-ttu-id="8d0d8-234">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-234">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-235">**Description**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-235">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-238">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-238">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-239">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-239">Textual description of the object.</span></span>

<span data-ttu-id="8d0d8-240">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-241">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-241">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-244">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-244">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-245">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-245">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="8d0d8-246">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-246">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-247">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="8d0d8-247">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-248">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-248">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-251">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-251">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-252">Nom de fichier compatible DOS.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-252">DOS-compatible file name.</span></span> <span data-ttu-id="8d0d8-253">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-254">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="8d0d8-254">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-255">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-255">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-256">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-258">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-258">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-259">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-259">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="8d0d8-260">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-260">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-261">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-261">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-262">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-264">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-264">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-265">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-265">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="8d0d8-266">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-266">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="8d0d8-267">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-267">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="8d0d8-268">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="8d0d8-268">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="8d0d8-269">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-269">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-270">**Extension**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-270">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-273">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-273">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-274">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-274">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="8d0d8-275">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-275">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-276">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="8d0d8-276">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-277">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-277">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-280">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-280">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-281">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-281">File name without the file name extension.</span></span>

<span data-ttu-id="8d0d8-282">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-282">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-283">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="8d0d8-283">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-284">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-284">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-285">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-285">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-287">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-288">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-288">Size of the file, in bytes.</span></span>

<span data-ttu-id="8d0d8-289">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-289">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-290">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-290">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-291">**FileType**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-291">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-294">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-295">Descripteur qui représente le type de fichier (indiqué par la propriété d' **extension** ).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-295">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="8d0d8-296">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-296">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-297">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-297">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-300">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-300">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-301">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-301">Class of the file system.</span></span>

<span data-ttu-id="8d0d8-302">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-302">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-303">**FSName**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-303">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-306">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-306">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-307">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-307">Name of the file system.</span></span>

<span data-ttu-id="8d0d8-308">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-309">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-309">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-310">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-312">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-312">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-313">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-313">If **True**, the file is hidden.</span></span>

<span data-ttu-id="8d0d8-314">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-314">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-315">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-315">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-316">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-316">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-318">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-319">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-319">Date and time when the object was installed.</span></span> <span data-ttu-id="8d0d8-320">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-320">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8d0d8-321">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-322">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-322">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-323">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-325">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-326">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-326">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="8d0d8-327">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-328">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-328">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-329">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-329">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-330">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-332">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-332">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-333">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-333">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="8d0d8-334">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-334">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-335">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-335">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-336">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-338">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-338">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-339">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-339">Date and time that the file was last modified.</span></span>

<span data-ttu-id="8d0d8-340">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-340">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-341">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-344">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-344">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-345">Nom hérité qui sert de clé d’une instance de fichier logique dans un système de fichiers (fournir des noms de chemin d’accès complet).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-345">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="8d0d8-346">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8d0d8-347">Exemple : « C : \\ \\ système Windows \\win.ini »</span><span class="sxs-lookup"><span data-stu-id="8d0d8-347">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-348">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-348">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-351">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-351">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-352">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-352">Path of the file including the leading and trailing backslashes.</span></span> <span data-ttu-id="8d0d8-353">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-354">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="8d0d8-354">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-355">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-355">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-356">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-358">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-359">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-359">If **True**, the file can be read.</span></span>

<span data-ttu-id="8d0d8-360">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-360">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-361">**État**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-362">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-364">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-364">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-365">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-365">String that indicates the current status of the object.</span></span>

<span data-ttu-id="8d0d8-366">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8d0d8-367">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d0d8-367">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8d0d8-368">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-368">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8d0d8-369">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-369">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8d0d8-370">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-370">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8d0d8-371">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="8d0d8-371">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8d0d8-372">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-372">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8d0d8-373">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-373">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8d0d8-374">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-374">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8d0d8-375">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-375">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8d0d8-376">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-376">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8d0d8-377">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-377">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8d0d8-378">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-378">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8d0d8-379">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-379">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8d0d8-380">**Système**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-380">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-381">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-383">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-384">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-384">If **True**, the file is a system file.</span></span>

<span data-ttu-id="8d0d8-385">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-385">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d0d8-386">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-386">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d0d8-387">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8d0d8-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d0d8-389">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="8d0d8-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="8d0d8-390">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-390">If **True**, the file can be written.</span></span>

<span data-ttu-id="8d0d8-391">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-391">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d0d8-392">Notes</span><span class="sxs-lookup"><span data-stu-id="8d0d8-392">Remarks</span></span>

<span data-ttu-id="8d0d8-393">La classe de **\_ répertoire CIM** est dérivée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-393">The **CIM\_Directory** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="8d0d8-394">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-394">WMI does not implement this class.</span></span> <span data-ttu-id="8d0d8-395">Pour plus d’informations sur les classes dérivées du **\_ répertoire CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8d0d8-395">For more information about classes derived from **CIM\_Directory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8d0d8-396">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-396">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d0d8-397">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8d0d8-397">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d0d8-398">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d0d8-398">Requirements</span></span>



| <span data-ttu-id="8d0d8-399">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d0d8-399">Requirement</span></span> | <span data-ttu-id="8d0d8-400">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d0d8-400">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d0d8-401">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d0d8-401">Minimum supported client</span></span><br/> | <span data-ttu-id="8d0d8-402">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d0d8-402">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d0d8-403">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d0d8-403">Minimum supported server</span></span><br/> | <span data-ttu-id="8d0d8-404">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d0d8-404">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d0d8-405">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d0d8-405">Namespace</span></span><br/>                | <span data-ttu-id="8d0d8-406">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8d0d8-406">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d0d8-407">MOF</span><span class="sxs-lookup"><span data-stu-id="8d0d8-407">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d0d8-408"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d0d8-408"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d0d8-409">DLL</span><span class="sxs-lookup"><span data-stu-id="8d0d8-409">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d0d8-410"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d0d8-410"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d0d8-411">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d0d8-411">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d0d8-412">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="8d0d8-412">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

