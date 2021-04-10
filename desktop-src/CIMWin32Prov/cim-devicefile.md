---
description: La \_ classe CIM DeviceFile représente un type de fichier logique, qui représente un périphérique.
ms.assetid: b07f039c-8ab0-4e13-96d5-3621da19e66d
ms.tgt_platform: multiple
title: Classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile
- CIM_DeviceFile.AccessMask
- CIM_DeviceFile.Archive
- CIM_DeviceFile.Caption
- CIM_DeviceFile.Compressed
- CIM_DeviceFile.CompressionMethod
- CIM_DeviceFile.CreationClassName
- CIM_DeviceFile.CreationDate
- CIM_DeviceFile.CSCreationClassName
- CIM_DeviceFile.CSName
- CIM_DeviceFile.Description
- CIM_DeviceFile.Drive
- CIM_DeviceFile.EightDotThreeFileName
- CIM_DeviceFile.Encrypted
- CIM_DeviceFile.EncryptionMethod
- CIM_DeviceFile.Extension
- CIM_DeviceFile.FileName
- CIM_DeviceFile.FileSize
- CIM_DeviceFile.FileType
- CIM_DeviceFile.FSCreationClassName
- CIM_DeviceFile.FSName
- CIM_DeviceFile.Hidden
- CIM_DeviceFile.InstallDate
- CIM_DeviceFile.InUseCount
- CIM_DeviceFile.LastAccessed
- CIM_DeviceFile.LastModified
- CIM_DeviceFile.Name
- CIM_DeviceFile.Path
- CIM_DeviceFile.Readable
- CIM_DeviceFile.Status
- CIM_DeviceFile.System
- CIM_DeviceFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 476f0ecd212247e1fc96db3efedcc0c18a6a2e06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950726"
---
# <a name="cim_devicefile-class"></a><span data-ttu-id="5233b-103">\_Classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="5233b-103">CIM\_DeviceFile class</span></span>

<span data-ttu-id="5233b-104">La classe **CIM \_ DeviceFile** représente un type de fichier logique, qui représente un périphérique.</span><span class="sxs-lookup"><span data-stu-id="5233b-104">The **CIM\_DeviceFile** class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="5233b-105">Cette Convention est utile pour les systèmes d’exploitation qui gèrent des appareils à l’aide d’un modèle d’e/s de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="5233b-105">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="5233b-106">L’appareil logique associé à ce fichier est spécifié à l’aide de la relation [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="5233b-106">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5233b-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5233b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5233b-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5233b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5233b-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5233b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5233b-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5233b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5233b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5233b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{4333BD60-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceFile : CIM_LogicalFile
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

## <a name="members"></a><span data-ttu-id="5233b-112">Membres</span><span class="sxs-lookup"><span data-stu-id="5233b-112">Members</span></span>

<span data-ttu-id="5233b-113">La classe **CIM \_ DeviceFile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5233b-113">The **CIM\_DeviceFile** class has these types of members:</span></span>

-   [<span data-ttu-id="5233b-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5233b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5233b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5233b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5233b-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5233b-116">Methods</span></span>

<span data-ttu-id="5233b-117">La classe **CIM \_ DeviceFile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5233b-117">The **CIM\_DeviceFile** class has these methods.</span></span>



| <span data-ttu-id="5233b-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="5233b-118">Method</span></span>                                                                                            | <span data-ttu-id="5233b-119">Description</span><span class="sxs-lookup"><span data-stu-id="5233b-119">Description</span></span>                                                                                                                                              |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5233b-120">**ChangeSecurityPermissions**</span><span class="sxs-lookup"><span data-stu-id="5233b-120">**ChangeSecurityPermissions**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)     | <span data-ttu-id="5233b-121">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-121">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="5233b-122">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-122">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="5233b-123">**ChangeSecurityPermissionsEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-123">**ChangeSecurityPermissionsEx**</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md) | <span data-ttu-id="5233b-124">Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-124">Changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="5233b-125">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-125">Not implemented by WMI.</span></span><br/>                                   |
| [<span data-ttu-id="5233b-126">**Dens**</span><span class="sxs-lookup"><span data-stu-id="5233b-126">**Compress**</span></span>](compress-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="5233b-127">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-127">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-128">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-128">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="5233b-129">**CompressEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-129">**CompressEx**</span></span>](compressex-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="5233b-130">Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-130">Compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-131">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-131">Not implemented by WMI.</span></span><br/>                                              |
| [<span data-ttu-id="5233b-132">**Copier**</span><span class="sxs-lookup"><span data-stu-id="5233b-132">**Copy**</span></span>](copy-method-in-class-cim-devicefile.md)                                               | <span data-ttu-id="5233b-133">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5233b-133">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="5233b-134">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-134">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="5233b-135">**CopyEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-135">**CopyEx**</span></span>](copyex-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5233b-136">Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5233b-136">Copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="5233b-137">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-137">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="5233b-138">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="5233b-138">**Delete**</span></span>](delete-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5233b-139">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-139">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-140">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-140">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5233b-141">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-141">**DeleteEx**</span></span>](deleteex-method-in-class-cim-devicefile.md)                                       | <span data-ttu-id="5233b-142">Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-142">Deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-143">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-143">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5233b-144">**GetEffectivePermission**</span><span class="sxs-lookup"><span data-stu-id="5233b-144">**GetEffectivePermission**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)           | <span data-ttu-id="5233b-145">Détermine si l’appelant dispose des autorisations agrégées spécifiées par l’argument d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="5233b-145">Determines whether the caller has the aggregated permissions specified by the **Permission** argument.</span></span> <span data-ttu-id="5233b-146">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-146">Not implemented by WMI.</span></span><br/>                |
| [<span data-ttu-id="5233b-147">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="5233b-147">**Rename**</span></span>](rename-method-in-class-cim-devicefile.md)                                           | <span data-ttu-id="5233b-148">Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-148">Renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-149">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-149">Not implemented by WMI.</span></span><br/>                                                 |
| [<span data-ttu-id="5233b-150">**TakeOwnerShip**</span><span class="sxs-lookup"><span data-stu-id="5233b-150">**TakeOwnerShip**</span></span>](takeownership-method-in-class-cim-devicefile.md)                             | <span data-ttu-id="5233b-151">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-151">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5233b-152">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-152">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="5233b-153">**TakeOwnerShipEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-153">**TakeOwnerShipEx**</span></span>](takeownershipex-method-in-class-cim-devicefile.md)                         | <span data-ttu-id="5233b-154">Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-154">Obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5233b-155">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-155">Not implemented by WMI.</span></span><br/>                                                   |
| [<span data-ttu-id="5233b-156">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="5233b-156">**Uncompress**</span></span>](uncompress-method-in-class-cim-devicefile.md)                                   | <span data-ttu-id="5233b-157">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-157">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-158">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-158">Not implemented by WMI.</span></span><br/>                                            |
| [<span data-ttu-id="5233b-159">**UncompressEx**</span><span class="sxs-lookup"><span data-stu-id="5233b-159">**UncompressEx**</span></span>](uncompressex-method-in-class-cim-devicefile.md)                               | <span data-ttu-id="5233b-160">Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-160">Uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5233b-161">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="5233b-161">Not implemented by WMI.</span></span><br/>                                            |



 

### <a name="properties"></a><span data-ttu-id="5233b-162">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5233b-162">Properties</span></span>

<span data-ttu-id="5233b-163">La classe **CIM \_ DeviceFile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5233b-163">The **CIM\_DeviceFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5233b-164">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="5233b-164">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5233b-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-167">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)</span><span class="sxs-lookup"><span data-stu-id="5233b-167">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-168">Tableau de bits qui représente les droits d’accès au fichier ou répertoire donné détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.</span><span class="sxs-lookup"><span data-stu-id="5233b-168">Bit array that represents the access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="5233b-169">Sur les volumes FAT, l' **\_ accès complet** est retourné, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-169">On FAT volumes, **FULL\_ACCESS** is returned, which indicates that no security has been set on the object.</span></span>

<span data-ttu-id="5233b-170">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-170">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5233b-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="5233b-171"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-172">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-172">Grants the right to read data from the file.</span></span> <span data-ttu-id="5233b-173">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="5233b-173">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="5233b-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="5233b-174"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-175">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-175">Grants the right to write data to the file.</span></span> <span data-ttu-id="5233b-176">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="5233b-176">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5233b-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="5233b-177"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-178">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-178">Grants the right to append data to the file.</span></span> <span data-ttu-id="5233b-179">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="5233b-179">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="5233b-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="5233b-180"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-181">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="5233b-181">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="5233b-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="5233b-182"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-183">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="5233b-183">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="5233b-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="5233b-184"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-185">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-185">Grants the right to execute a file.</span></span> <span data-ttu-id="5233b-186">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="5233b-186">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="5233b-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="5233b-187"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-188">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5233b-188">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="5233b-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="5233b-189"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-190">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-190">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="5233b-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="5233b-191"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-192">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-192">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="5233b-193"><span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="5233b-193"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-194">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="5233b-194">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="5233b-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="5233b-195"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-196">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="5233b-196">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="5233b-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="5233b-197"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-198">Octroie l’accès en écriture à la liste de contrôle d’accès discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="5233b-198">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="5233b-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="5233b-199"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-200">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="5233b-200">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="5233b-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="5233b-201"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="5233b-202">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="5233b-202">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5233b-203">**Archive**</span><span class="sxs-lookup"><span data-stu-id="5233b-203">**Archive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-204">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-206">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)</span><span class="sxs-lookup"><span data-stu-id="5233b-206">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-207">Si la **valeur est true**, le fichier doit être archivé.</span><span class="sxs-lookup"><span data-stu-id="5233b-207">If **True**, the file should be archived.</span></span>

<span data-ttu-id="5233b-208">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-208">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-209">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5233b-209">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-212">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="5233b-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-213">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-213">Short textual description of the object.</span></span>

<span data-ttu-id="5233b-214">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-215">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="5233b-215">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-218">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)</span><span class="sxs-lookup"><span data-stu-id="5233b-218">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-219">Si la **valeur est true**, le fichier est compressé.</span><span class="sxs-lookup"><span data-stu-id="5233b-219">If **True**, the file is compressed.</span></span>

<span data-ttu-id="5233b-220">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-220">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-221">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="5233b-221">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-224">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)</span><span class="sxs-lookup"><span data-stu-id="5233b-224">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compression Method")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-225">Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="5233b-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="5233b-226">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="5233b-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="5233b-227">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="5233b-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="5233b-228">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="5233b-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="5233b-229">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-229">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-230">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5233b-230">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-233">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="5233b-233">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-234">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="5233b-234">Name of the class.</span></span>

<span data-ttu-id="5233b-235">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-235">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-236">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="5233b-236">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-237">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5233b-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-239">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")</span><span class="sxs-lookup"><span data-stu-id="5233b-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Creation Date")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-240">Date de création du fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-240">File's creation date.</span></span>

<span data-ttu-id="5233b-241">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-241">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-242">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5233b-242">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-245">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="5233b-245">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-246">Classe du système informatique.</span><span class="sxs-lookup"><span data-stu-id="5233b-246">Class of the computer system.</span></span>

<span data-ttu-id="5233b-247">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-247">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-248">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5233b-248">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-251">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")</span><span class="sxs-lookup"><span data-stu-id="5233b-251">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-252">Nom du système informatique.</span><span class="sxs-lookup"><span data-stu-id="5233b-252">Name of the computer system.</span></span>

<span data-ttu-id="5233b-253">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-253">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-254">**Description**</span><span class="sxs-lookup"><span data-stu-id="5233b-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-257">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="5233b-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-258">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-258">Textual description of the object.</span></span>

<span data-ttu-id="5233b-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-260">**Lecteur**</span><span class="sxs-lookup"><span data-stu-id="5233b-260">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-263">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span><span class="sxs-lookup"><span data-stu-id="5233b-263">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-264">Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-264">Drive letter (including the colon that follows the drive letter) of the file.</span></span> <span data-ttu-id="5233b-265">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-265">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-266">Exemple : "c :"</span><span class="sxs-lookup"><span data-stu-id="5233b-266">Example: "c:"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-267">**EightDotThreeFileName**</span><span class="sxs-lookup"><span data-stu-id="5233b-267">**EightDotThreeFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-270">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")</span><span class="sxs-lookup"><span data-stu-id="5233b-270">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-271">Nom de fichier compatible DOS pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-271">DOS-compatible file name for the file.</span></span> <span data-ttu-id="5233b-272">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-272">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-273">Exemple : « c : \\ PROGRA ~ 1 »</span><span class="sxs-lookup"><span data-stu-id="5233b-273">Example: "c:\\progra~1"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-274">**Chiffré**</span><span class="sxs-lookup"><span data-stu-id="5233b-274">**Encrypted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-275">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-277">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span><span class="sxs-lookup"><span data-stu-id="5233b-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-278">Si la **valeur est true**, le fichier est chiffré.</span><span class="sxs-lookup"><span data-stu-id="5233b-278">If **True**, the file is encrypted.</span></span>

<span data-ttu-id="5233b-279">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-279">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-280">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="5233b-280">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-283">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)</span><span class="sxs-lookup"><span data-stu-id="5233b-283">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encryption Method")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-284">Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique.</span><span class="sxs-lookup"><span data-stu-id="5233b-284">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="5233b-285">Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="5233b-285">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="5233b-286">Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="5233b-286">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="5233b-287">Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».</span><span class="sxs-lookup"><span data-stu-id="5233b-287">If the logical file is not encrypted, use "Not Encrypted".</span></span>

<span data-ttu-id="5233b-288">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-288">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-289">**Extension**</span><span class="sxs-lookup"><span data-stu-id="5233b-289">**Extension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-290">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-292">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")</span><span class="sxs-lookup"><span data-stu-id="5233b-292">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-293">Extension de nom de fichier sans le point précédent (point).</span><span class="sxs-lookup"><span data-stu-id="5233b-293">File name extension without the preceding period (dot).</span></span>

<span data-ttu-id="5233b-294">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-294">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-295">Exemple : "txt", "MOF", "mdb"</span><span class="sxs-lookup"><span data-stu-id="5233b-295">Example: "txt", "mof", "mdb"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-296">**FileName**</span><span class="sxs-lookup"><span data-stu-id="5233b-296">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-299">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")</span><span class="sxs-lookup"><span data-stu-id="5233b-299">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-300">Nom de fichier sans l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-300">File name without the file name extension.</span></span>

<span data-ttu-id="5233b-301">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-301">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-302">Exemple : « MyDataFile »</span><span class="sxs-lookup"><span data-stu-id="5233b-302">Example: "MyDataFile"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-303">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="5233b-303">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-304">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5233b-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-306">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)</span><span class="sxs-lookup"><span data-stu-id="5233b-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-307">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="5233b-307">Size of the file, in bytes.</span></span>

<span data-ttu-id="5233b-308">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-308">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-309">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5233b-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-310">**FileType**</span><span class="sxs-lookup"><span data-stu-id="5233b-310">**FileType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-313">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")</span><span class="sxs-lookup"><span data-stu-id="5233b-313">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-314">Descripteur qui représente le type de fichier (indiqué par la propriété d' **extension** ).</span><span class="sxs-lookup"><span data-stu-id="5233b-314">Descriptor that represents the file type (indicated by the **Extension** property).</span></span>

<span data-ttu-id="5233b-315">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-315">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-316">**FSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5233b-316">**FSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-317">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-319">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="5233b-319">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-320">Classe du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5233b-320">Class of the file system.</span></span>

<span data-ttu-id="5233b-321">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-321">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-322">**FSName**</span><span class="sxs-lookup"><span data-stu-id="5233b-322">**FSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-325">Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")</span><span class="sxs-lookup"><span data-stu-id="5233b-325">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-326">Nom du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="5233b-326">Name of the file system.</span></span>

<span data-ttu-id="5233b-327">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-327">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-328">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="5233b-328">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-329">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-331">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)</span><span class="sxs-lookup"><span data-stu-id="5233b-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-332">Si la **valeur est true**, le fichier est masqué.</span><span class="sxs-lookup"><span data-stu-id="5233b-332">If **True**, the file is hidden.</span></span>

<span data-ttu-id="5233b-333">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-333">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5233b-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-335">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5233b-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="5233b-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-338">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-338">Date and time when the object was installed.</span></span> <span data-ttu-id="5233b-339">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="5233b-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5233b-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-341">**InUseCount**</span><span class="sxs-lookup"><span data-stu-id="5233b-341">**InUseCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5233b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-344">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)</span><span class="sxs-lookup"><span data-stu-id="5233b-344">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-345">Nombre de « ouvertures de fichier » actuellement actives sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-345">Number of "file opens" that are currently active against the file.</span></span>

<span data-ttu-id="5233b-346">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-346">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-347">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5233b-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-348">**LastAccessed**</span><span class="sxs-lookup"><span data-stu-id="5233b-348">**LastAccessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-349">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5233b-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-351">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)</span><span class="sxs-lookup"><span data-stu-id="5233b-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Accessed")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-352">Date et heure du dernier accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-352">Date and time that the file was last accessed.</span></span>

<span data-ttu-id="5233b-353">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-353">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-354">**LastModified**</span><span class="sxs-lookup"><span data-stu-id="5233b-354">**LastModified**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-355">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5233b-355">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-357">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)</span><span class="sxs-lookup"><span data-stu-id="5233b-357">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Last Modified")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-358">Date et heure de la dernière modification du fichier.</span><span class="sxs-lookup"><span data-stu-id="5233b-358">Date and time that the file was last modified.</span></span>

<span data-ttu-id="5233b-359">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-359">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-360">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5233b-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-363">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5233b-363">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5233b-364">Nom hérité qui sert de clé d’une instance de fichier logique dans un système de fichiers (fournir des noms de chemin d’accès complet).</span><span class="sxs-lookup"><span data-stu-id="5233b-364">Inherited name that serves as a key of a logical file instance within a file system (provide full path names).</span></span>

<span data-ttu-id="5233b-365">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5233b-366">Exemple : « C : \\ \\ système Windows \\win.ini »</span><span class="sxs-lookup"><span data-stu-id="5233b-366">Example: "C:\\Windows\\system\\win.ini"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-367">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="5233b-367">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-370">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")</span><span class="sxs-lookup"><span data-stu-id="5233b-370">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-371">Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="5233b-371">Path of the file including leading and trailing backslashes.</span></span> <span data-ttu-id="5233b-372">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-372">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-373">Exemple : « \\ \\ système Windows \\ »</span><span class="sxs-lookup"><span data-stu-id="5233b-373">Example: "\\windows\\system\\"</span></span>

</dd> <dt>

<span data-ttu-id="5233b-374">**R.a.**</span><span class="sxs-lookup"><span data-stu-id="5233b-374">**Readable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-375">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-377">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")</span><span class="sxs-lookup"><span data-stu-id="5233b-377">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-378">Si la **valeur est true**, le fichier peut être lu.</span><span class="sxs-lookup"><span data-stu-id="5233b-378">If **True**, the file can be read.</span></span>

<span data-ttu-id="5233b-379">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-379">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-380">**État**</span><span class="sxs-lookup"><span data-stu-id="5233b-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5233b-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-383">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="5233b-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-384">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5233b-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="5233b-385">L’état opérationnel et l’état des opérations ne peuvent pas être définis.</span><span class="sxs-lookup"><span data-stu-id="5233b-385">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="5233b-386">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="5233b-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5233b-387">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="5233b-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5233b-388">L’état de fonctionnement peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5233b-388">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5233b-389">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5233b-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5233b-390">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5233b-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5233b-391">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5233b-392">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5233b-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5233b-393">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="5233b-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5233b-394">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="5233b-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5233b-395">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5233b-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5233b-396">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="5233b-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5233b-397">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5233b-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5233b-398">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5233b-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5233b-399">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5233b-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5233b-400">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="5233b-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5233b-401">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="5233b-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5233b-402">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="5233b-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5233b-403">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="5233b-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5233b-404">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="5233b-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5233b-405">**Système**</span><span class="sxs-lookup"><span data-stu-id="5233b-405">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-406">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-408">Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)</span><span class="sxs-lookup"><span data-stu-id="5233b-408">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-409">Si la **valeur est true**, le fichier est un fichier système.</span><span class="sxs-lookup"><span data-stu-id="5233b-409">If **True**, the file is a system file.</span></span>

<span data-ttu-id="5233b-410">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-410">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5233b-411">**Inscriptible**</span><span class="sxs-lookup"><span data-stu-id="5233b-411">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5233b-412">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5233b-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5233b-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5233b-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5233b-414">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)</span><span class="sxs-lookup"><span data-stu-id="5233b-414">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")</span></span>
</dt> </dl>

<span data-ttu-id="5233b-415">Si la **valeur est true**, le fichier peut être écrit.</span><span class="sxs-lookup"><span data-stu-id="5233b-415">If **True**, the file can be written.</span></span>

<span data-ttu-id="5233b-416">Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-416">This property is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5233b-417">Notes</span><span class="sxs-lookup"><span data-stu-id="5233b-417">Remarks</span></span>

<span data-ttu-id="5233b-418">La classe **CIM \_ DeviceFile** est dérivée de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5233b-418">The **CIM\_DeviceFile** class is derived from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

<span data-ttu-id="5233b-419">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="5233b-419">WMI does not implement this class.</span></span>

<span data-ttu-id="5233b-420">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5233b-420">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5233b-421">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5233b-421">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5233b-422">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5233b-422">Requirements</span></span>



| <span data-ttu-id="5233b-423">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5233b-423">Requirement</span></span> | <span data-ttu-id="5233b-424">Valeur</span><span class="sxs-lookup"><span data-stu-id="5233b-424">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5233b-425">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5233b-425">Minimum supported client</span></span><br/> | <span data-ttu-id="5233b-426">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5233b-426">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5233b-427">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5233b-427">Minimum supported server</span></span><br/> | <span data-ttu-id="5233b-428">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5233b-428">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5233b-429">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5233b-429">Namespace</span></span><br/>                | <span data-ttu-id="5233b-430">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5233b-430">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5233b-431">MOF</span><span class="sxs-lookup"><span data-stu-id="5233b-431">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5233b-432"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5233b-432"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5233b-433">DLL</span><span class="sxs-lookup"><span data-stu-id="5233b-433">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5233b-434"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5233b-434"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5233b-435">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5233b-435">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5233b-436">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="5233b-436">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

