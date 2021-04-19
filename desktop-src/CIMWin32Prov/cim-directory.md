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
# <a name="cim_directory-class"></a>\_Classe de répertoire CIM

La classe de **\_ répertoire CIM** représente un type de fichier qui regroupe logiquement les fichiers de données qu’elle contient et fournit des informations de chemin d’accès pour les fichiers groupés.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe de **\_ répertoire CIM** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ répertoire CIM** possède ces méthodes.



| Méthode                                                                                           | Description                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md)     | Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-directory.md) | Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                   |
| [**Dens**](compress-method-in-class-cim-directory.md)                                       | Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-directory.md)                                   | Compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                              |
| [**Copier**](copy-method-in-class-cim-directory.md)                                               | Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée. Non implémenté par WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-directory.md)                                           | Copie le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée. Non implémenté par WMI.<br/> |
| [**Supprimer**](delete-method-in-class-cim-directory.md)                                           | Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-directory.md)                                       | Supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-directory.md)           | Détermine si l’appelant dispose des autorisations agrégées spécifiées par l’argument d' **autorisation** . Non implémenté par WMI.<br/>                |
| [**Renommer**](rename-method-in-class-cim-directory.md)                                           | Renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md)                             | Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md)                         | Obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                                   |
| [**Décompresser**](uncompress-method-in-class-cim-directory.md)                                   | Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-directory.md)                               | Décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Non implémenté par WMI.<br/>                                            |



 

### <a name="properties"></a>Propriétés

La classe de **\_ répertoire CIM** possède ces propriétés.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)
</dt> </dl>

Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur l’annuaire. Pour obtenir les valeurs, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.

 

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**Fichier \_ LIRE \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**Fichier \_ ÉCRIRE \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**Fichier \_ \_Attributs de lecture** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**Fichier \_ \_Attributs d’écriture** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Supprimer** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Lecture \_ CONTRÔLE** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Écriture \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Écriture \_ PROPRIÉTAIRE** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Synchroniser** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archive**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)
</dt> </dl>

Si la **valeur est true**, le fichier doit être archivé.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)
</dt> </dl>

Courte description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« compressé »)
</dt> </dl>

Si la **valeur est true**, le fichier est compressé.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de compression »)
</dt> </dl>

Chaîne de forme libre qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique. Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ». Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ». Si le fichier logique n’est pas compressé, utilisez « non compressé ».

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")
</dt> </dl>

Nom de la classe.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("date de création")
</dt> </dl>

Date et heure de création du fichier.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Class Name ")
</dt> </dl>

Classe du système informatique.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CSName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de l’ordinateur ")
</dt> </dl>

Nom du système informatique.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Description textuelle de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Lecteur**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Lettre de lecteur (y compris le signe deux-points qui suit la lettre de lecteur) du fichier. Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Exemple : "c :"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")
</dt> </dl>

Nom de fichier compatible DOS. Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Exemple : « c : \\ PROGRA ~ 1 »

</dd> <dt>

**Chiffré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Si la **valeur est true**, le fichier est chiffré.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« méthode de chiffrement »)
</dt> </dl>

Chaîne de forme libre qui identifie l’algorithme ou l’outil utilisé pour chiffrer un fichier logique. Si le schéma de chiffrement n’est pas indulged (pour des raisons de sécurité, par exemple), utilisez « inconnu ». Si le fichier est chiffré, mais que son schéma de chiffrement est inconnu ou non divulgué, utilisez « chiffré ». Si le fichier logique n’est pas chiffré, utilisez « non chiffré ».

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Extension**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extension de fichier")
</dt> </dl>

Extension de nom de fichier sans le point précédent (point).

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Exemple : "txt", "MOF", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")
</dt> </dl>

Nom de fichier sans l’extension de nom de fichier.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Exemple : « MyDataFile »

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)
</dt> </dl>

Taille du fichier en octets.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")
</dt> </dl>

Descripteur qui représente le type de fichier (indiqué par la propriété d' **extension** ).

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom de la classe du système de fichiers ")
</dt> </dl>

Classe du système de fichiers.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**propagés**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système de fichiers CIM**](cim-filesystem.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nom du système de fichiers ")
</dt> </dl>

Nom du système de fichiers.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Hidden**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« masqué »)
</dt> </dl>

Si la **valeur est true**, le fichier est masqué.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")
</dt> </dl>

Date et heure d’installation de l’objet. Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« nombre actuel de fichiers ouverts »)
</dt> </dl>

Nombre de « ouvertures de fichier » actuellement actives sur le fichier.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« dernier accès »)
</dt> </dl>

Date et heure du dernier accès au fichier.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Last modified »)
</dt> </dl>

Date et heure de la dernière modification du fichier.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nom hérité qui sert de clé d’une instance de fichier logique dans un système de fichiers (fournir des noms de chemin d’accès complet).

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Exemple : « C : \\ \\ système Windows \\win.ini »

</dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")
</dt> </dl>

Chemin d’accès du fichier, y compris les barres obliques inverses de début et de fin. Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

Exemple : « \\ \\ système Windows \\ »

</dd> <dt>

**R.a.**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")
</dt> </dl>

Si la **valeur est true**, le fichier peut être lu.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**État**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Chaîne qui indique l’état actuel de l’objet.

Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Les valeurs sont notamment les suivantes :

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (« OK »)


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erreur** (« erreur »)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Détérioré** (« détérioré »)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** ("inconnu")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Échec** prévu (« échec prédit »)


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Démarrage** en cours (« démarrage »)


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arrêt** en cours (« arrêt »)


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** (« service »)


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** (« stressed »)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Non **récupéré** (« non récupéré »)


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Aucun contact** (« aucun contact »)


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Communication perdue** (« inversée comm »)


</dt> <dd></dd> </dl>

</dd> <dt>

**Système**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« fichier système »)
</dt> </dl>

Si la **valeur est true**, le fichier est un fichier système.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Inscriptible**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« inscriptible »)
</dt> </dl>

Si la **valeur est true**, le fichier peut être écrit.

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Notes

La classe de **\_ répertoire CIM** est dérivée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

WMI n’implémente pas cette classe. Pour plus d’informations sur les classes dérivées du **\_ répertoire CIM**, consultez [classes Win32](win32-provider.md).

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

