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
# <a name="win32_directory-class"></a>\_Classe de répertoire Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l' **\_ Annuaire Win32** représente une entrée de répertoire sur un système informatique exécutant Windows. Un répertoire est un type de fichier qui regroupe logiquement des fichiers de données et fournit des informations de chemin d’accès pour les fichiers groupés. Exemple : C : \\ temp. **Win32 \_ Le répertoire** n’inclut pas les répertoires des lecteurs réseau.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe de **\_ répertoire win32** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ répertoire win32** possède ces méthodes.



| Méthode                                                                                             | Description                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)     | Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                        |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Méthode de classe qui modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                        |
| [**Dens**](compress-method-in-class-win32-directory.md)                                       | Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | Méthode de classe qui compresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                   |
| [**Copier**](copy-method-in-class-win32-directory.md)                                               | Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | Méthode de classe qui copie le fichier logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .<br/>                                                                                   |
| [**Supprimer**](delete-method-in-class-win32-directory.md)                                           | Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | Méthode de classe qui supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                      |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-directory.md)           | Méthode de classe qui détermine si l’appelant a les autorisations agrégées spécifiées par l’argument d' *autorisation* non seulement sur l’objet de fichier, mais sur le partage sur lequel le fichier ou le répertoire réside (s’il se trouve sur un partage).<br/> |
| [**Renommer**](rename-method-in-class-win32-directory.md)                                           | Méthode de classe qui renomme le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                      |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md)                             | Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                        |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-directory.md)                         | Méthode de classe qui obtient la propriété du fichier logique spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                        |
| [**Décompresser**](uncompress-method-in-class-win32-directory.md)                                   | Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                 |
| [**UncompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Méthode de classe qui décompresse le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Propriétés

La classe de **\_ répertoire win32** possède ces propriétés.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« droits d’accès »)
</dt> </dl>

Masque binaire qui représente les droits d’accès requis pour accéder ou effectuer des opérations spécifiques sur l’annuaire. Pour les valeurs de bit, consultez [**constantes de droits d’accès aux fichiers et aux répertoires**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.

 

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)


</dt> <dd>

Accorde le droit de lire des données à partir du fichier. Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)


</dt> <dd>

Accorde le droit d’écrire des données dans le fichier. Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Fichier \_ Ajouter des \_ données (fichier) ou \_ un \_ sous-répertoire d’ajout de fichier** (4)


</dt> <dd>

Accorde le droit d’ajouter des données au fichier. Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)


</dt> <dd>

Accorde le droit de lire les attributs étendus.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)


</dt> <dd>

Accorde le droit d’écrire des attributs étendus.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)


</dt> <dd>

Accorde le droit d’exécuter un fichier. Pour un répertoire, le répertoire peut être parcouru.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)


</dt> <dd>

Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)


</dt> <dd>

Accorde le droit de lire les attributs du fichier.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)


</dt> <dd>

Accorde le droit de modifier les attributs de fichier.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)


</dt> <dd>

Octroie l’accès en suppression.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)


</dt> <dd>

Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)


</dt> <dd>

Octroie l’accès en écriture à la liste de contrôle d’accès discrétionnaire.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)


</dt> <dd>

Affecte le propriétaire de l’écriture.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)


</dt> <dd>

Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Accès \_ \_Sécurité du système** (18809343)


</dt> <dd>

Contrôle la capacité à récupérer ou à définir la liste SACL dans le descripteur de sécurité d’un objet.

</dd> </dl>

</dd> <dt>

**Archive**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**schéma**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32 »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« doit être archivé »)
</dt> </dl>

Indique si le bit d’archive sur le dossier a été défini. Le bit d’archive est utilisé par les programmes de sauvegarde pour identifier les fichiers qui doivent être sauvegardés. Si la **valeur est true**, le fichier doit être archivé.

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

Brève description textuelle de l’objet.

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

Indique si le dossier a été compressé ou non. WMI reconnaît les dossiers compressés à l’aide de WMI lui-même ou à l’aide de l’interface utilisateur graphique ; Toutefois, elle ne reconnaît pas. Fichiers ZIP en cours de compression. Si la **valeur est true**, le fichier est compressé.

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

Algorithme ou outil (généralement une méthode) utilisé pour compresser le fichier logique. Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de compression (peut-être parce qu’il n’est pas connu), utilisez les mots suivants : « inconnu » pour indiquer qu’il n’est pas connu que le fichier logique est compressé ou non ; « Compressed » pour représenter le fait que le fichier est compressé, mais que son schéma de compression n’est pas connu ou qu’il n’est pas divulgué ; et « non compressés » pour indiquer que le fichier logique n’est pas compressé.

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

Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance. Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.

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

Date à laquelle l’objet système de fichiers a été créé. Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Nom de la classe de création du système d’étendue de l’ordinateur.

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

Nom de l’ordinateur où est stocké l’objet de système de fichiers.

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

Lettre de lecteur du lecteur (y compris les deux-points) dans laquelle l’objet de système de fichiers est stocké.

Exemple : "c :"

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("huit point trois nom de fichier")
</dt> </dl>

Nom compatible MS-DOS pour le dossier.

Exemple : « c : \\ PROGRA ~ 1 »

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Chiffré**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Indique si le dossier a été chiffré ou non. Si la **valeur est true**, le dossier est chiffré.

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

Algorithme ou outil utilisé pour chiffrer le fichier logique. Si ce n’est pas possible (ou n’est pas souhaité) de décrire le schéma de chiffrement (pour des raisons de sécurité, par exemple), utilisez les mots suivants : « inconnu » pour indiquer qu’il est impossible de savoir si le fichier logique est chiffré ; « Chiffré » pour représenter le chiffrement du fichier, mais son schéma de chiffrement n’est pas connu ou n’est pas divulgué ; et « non chiffrés » pour représenter le fait que le fichier logique n’est pas chiffré.

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

Extension de nom de fichier pour l’objet de système de fichiers, à l’exclusion du point (.) qui sépare l’extension du nom de fichier.

Exemples : "txt", "MOF", "mdb"

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file name")
</dt> </dl>

Nom de fichier (sans le point ou l’extension) du fichier.

Exemple : « Autoexec »

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Size »), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (« bytes »)
</dt> </dl>

Taille de l’objet système de fichiers, en octets. Bien que les dossiers possèdent une propriété **FileSize** , la valeur 0 est toujours retournée. Pour déterminer la taille d’un dossier, utilisez FileSystemObject ou ajoutez la taille de tous les fichiers stockés dans le dossier.

Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de fichier")
</dt> </dl>

Type de fichier (indiqué par la propriété d' **extension** ).

Par exemple, un fichier. mdb est susceptible d’avoir le type de fichier application Microsoft Access. Un fichier. asp a probablement le type de fichier document HTML. Les dossiers sont généralement signalés simplement comme dossiers.

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

Type de système de fichiers (NTFS, FAT, FAT32) installé sur le lecteur où se trouve le fichier ou le dossier.

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

Indique si l’objet de système de fichiers est masqué. Si la **valeur est true**, le fichier est masqué.

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

Indique le moment où l’objet a été installé. L’absence de valeur n’indique pas que l’objet n’est pas installé.

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

Date du dernier accès au fichier. Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Date de la dernière modification du fichier. Pour plus d’informations sur l’utilisation des formats de date et d’heure WMI, consultez [tâches WMI : dates et heures](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

La propriété Name est une chaîne représentant le nom hérité qui sert de clé à une instance de fichier logique dans un système de fichiers. Les noms de chemin d’accès complets doivent être fournis. Exemple : C : \\ \\ système Windows \\win.ini

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")
</dt> </dl>

Chemin d’accès du fichier. Le chemin d’accès comprend les barres obliques inverses de début et de fin, mais pas la lettre de lecteur ou le nom de dossier.

Pour le dossier c : \\ Windows \\ system32 \\ WBEM, le chemin d’accès est \\ Windows \\ system32 \\ . Pour le dossier c : \\ scripts, le chemin d’accès est \\ .

Cette propriété est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**R.a.**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("readed")
</dt> </dl>

Indique si vous pouvez lire des éléments dans le dossier. Si la **valeur est true**, le fichier peut être lu.

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

Indique si l’objet est un fichier système. Si la **valeur est true**, le fichier est un fichier système

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

La classe de **\_ répertoire win32** est dérivée du [**\_ répertoire CIM**](cim-directory.md).

**Vue d’ensemble**

Les dossiers sont des objets de système de fichiers conçus pour contenir d’autres objets de système de fichiers. Toutefois, cela ne signifie pas que tous les dossiers sont similaires. Au lieu de cela, les dossiers peuvent varier considérablement. Certains dossiers sont des dossiers du système d’exploitation, qui ne doivent généralement pas être modifiés par un script. Certains dossiers sont en lecture seule, ce qui signifie que les utilisateurs peuvent accéder au contenu de ce dossier, mais qu’ils ne peuvent pas ajouter, supprimer ou modifier ces contenus. Certains dossiers sont compressés pour un stockage optimal, tandis que d’autres sont masqués et invisibles pour les utilisateurs.

WMI utilise la classe de **\_ répertoire win32** pour gérer les dossiers. De manière significative, les propriétés et les méthodes disponibles dans cette classe sont identiques aux propriétés et aux méthodes disponibles dans la classe de [**\_ fichier de fichier CIM**](cim-datafile.md) , la classe utilisée pour gérer les fichiers. Cela signifie qu’une fois que vous avez appris à gérer des dossiers à l’aide de WMI, vous pouvez, sans aucun travail supplémentaire, savoir comment gérer les fichiers.

La classe d’association de [**\_ sous-répertoire win32**](win32-subdirectory.md) est également utilisée pour gérer des fichiers et des dossiers. La classe de **\_ sous-répertoire win32** lie un dossier et ses sous-dossiers immédiats. Par exemple, dans la structure de dossiers C : \\ scripts \\ journaux, logs est un sous-dossier de scripts et scripts est un sous-dossier du dossier racine C : \\ . Toutefois, les journaux ne sont pas considérés comme un sous-dossier de C : \\ .

Vous pouvez récupérer les propriétés de n’importe quel dossier dans le système de fichiers à l’aide de la classe de **\_ répertoire win32** . Les propriétés disponibles à l’aide de cette classe sont indiquées dans le tableau 11,1. Pour récupérer les propriétés d’un seul dossier, construisez une requête WQL (Windows Query Language) pour la classe de **\_ répertoire win32** , en veillant à inclure le nom du dossier. Par exemple, cette requête est liée au dossier D : \\ Archive :

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

Lorsque vous spécifiez un nom de fichier ou de dossier dans une requête WQL, veillez à utiliser deux barres obliques \\ \\ inverses () pour séparer les composants du chemin.

Si vous souhaitez limiter la récupération des données à un seul lecteur de disque, incluez une clause WHERE spécifiant la lettre de lecteur. Par exemple, cette requête renvoie une liste de tous les dossiers sur le lecteur C :

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Si vous devez énumérer tous les dossiers d’un ordinateur, sachez que cette requête peut prendre plus de temps.

## <a name="examples"></a>Exemples

L’exemple VBScript suivant récupère les propriétés du dossier C : \\ scripts.


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



L’exemple VBScript suivant retourne une liste de tous les dossiers masqués sur un ordinateur.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
```



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

[**\_Répertoire CIM**](cim-directory.md)
</dt> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

