---
description: Représente une connexion réseau active dans un environnement Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Classe Win32_NetworkConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748909"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="d8262-103">\_Classe NetworkConnection Win32</span><span class="sxs-lookup"><span data-stu-id="d8262-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="d8262-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection** WMI représente une connexion réseau active dans un environnement Windows.</span><span class="sxs-lookup"><span data-stu-id="d8262-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="d8262-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d8262-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d8262-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d8262-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8262-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8262-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="d8262-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d8262-108">Members</span></span>

<span data-ttu-id="d8262-109">La classe **Win32 \_ NetworkConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8262-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="d8262-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8262-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8262-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d8262-111">Properties</span></span>

<span data-ttu-id="d8262-112">La classe **Win32 \_ NetworkConnection** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8262-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8262-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="d8262-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d8262-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-116">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d8262-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-117">Liste des droits d’accès au fichier ou répertoire donné détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.</span><span class="sxs-lookup"><span data-stu-id="d8262-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="d8262-118">Sur les volumes FAT, la valeur d' **\_ accès complet** est retournée à la place, ce qui indique qu’aucune sécurité n’a été définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8262-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="d8262-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="d8262-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-120">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="d8262-121">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="d8262-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="d8262-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="d8262-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-123">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="d8262-124">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="d8262-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="d8262-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Fichier \_ Ajouter des \_ données (fichier) ou \_ un \_ sous-répertoire d’ajout de fichier** (4)</span><span class="sxs-lookup"><span data-stu-id="d8262-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-126">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="d8262-127">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="d8262-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="d8262-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="d8262-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-129">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="d8262-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="d8262-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="d8262-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-131">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="d8262-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="d8262-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="d8262-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-133">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-133">Grants the right to execute a file.</span></span> <span data-ttu-id="d8262-134">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="d8262-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="d8262-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="d8262-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-136">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d8262-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="d8262-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="d8262-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-138">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="d8262-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="d8262-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-140">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="d8262-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="d8262-141"><span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="d8262-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-142">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="d8262-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="d8262-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="d8262-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-144">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d8262-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="d8262-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="d8262-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-146">Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="d8262-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="d8262-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="d8262-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-148">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="d8262-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="d8262-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="d8262-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="d8262-150">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="d8262-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-151">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d8262-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-154">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d8262-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-155">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8262-155">A short textual description of the object.</span></span>

<span data-ttu-id="d8262-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8262-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8262-157">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="d8262-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-160">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")</span><span class="sxs-lookup"><span data-stu-id="d8262-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-161">Commentaire fourni par le fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="d8262-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="d8262-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-165">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api les \| structures de gestion de réseau \| [**utilisent \_ info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **Ui1 \_ Status**")</span><span class="sxs-lookup"><span data-stu-id="d8262-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-166">État actuel de la connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="d8262-167">**Connecté** (« connecté »)</span><span class="sxs-lookup"><span data-stu-id="d8262-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8262-168">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d8262-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d8262-169">**Suspendu** (« suspendu »)</span><span class="sxs-lookup"><span data-stu-id="d8262-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="d8262-170">**Déconnecté** (« déconnecté »)</span><span class="sxs-lookup"><span data-stu-id="d8262-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="d8262-171">**Connexion** (« connexion »)</span><span class="sxs-lookup"><span data-stu-id="d8262-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="d8262-172">**Reconnexion** (« reconnexion »)</span><span class="sxs-lookup"><span data-stu-id="d8262-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="d8262-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-176">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")</span><span class="sxs-lookup"><span data-stu-id="d8262-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-177">Type de persistance de la connexion utilisée pour la connexion au réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="d8262-178">**Connexion active** (« connexion en cours »)</span><span class="sxs-lookup"><span data-stu-id="d8262-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="d8262-179">**Connexion permanente** (« connexion persistante »)</span><span class="sxs-lookup"><span data-stu-id="d8262-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-180">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8262-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-183">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d8262-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-184">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8262-184">A textual description of the object.</span></span>

<span data-ttu-id="d8262-185">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8262-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8262-186">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="d8262-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-189">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")</span><span class="sxs-lookup"><span data-stu-id="d8262-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-190">L’objet réseau doit s’afficher dans une interface utilisateur de navigation réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="d8262-191">**Domaine** (« domaine »)</span><span class="sxs-lookup"><span data-stu-id="d8262-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="d8262-192">**Générique** (« Générique »)</span><span class="sxs-lookup"><span data-stu-id="d8262-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="d8262-193">**Serveur** (« serveur »)</span><span class="sxs-lookup"><span data-stu-id="d8262-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="d8262-194">**Partage** (« partage »)</span><span class="sxs-lookup"><span data-stu-id="d8262-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d8262-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-196">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d8262-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d8262-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-199">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="d8262-199">Indicates when the object was installed.</span></span> <span data-ttu-id="d8262-200">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="d8262-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d8262-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8262-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8262-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="d8262-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-205">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")</span><span class="sxs-lookup"><span data-stu-id="d8262-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-206">Nom local du périphérique réseau connecté.</span><span class="sxs-lookup"><span data-stu-id="d8262-206">Local name of the connected network device.</span></span>

<span data-ttu-id="d8262-207">Exemple : "c : \\ public"</span><span class="sxs-lookup"><span data-stu-id="d8262-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="d8262-208">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d8262-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-211">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("nom"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| structures réseau Windows win32api \| [](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="d8262-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-212">Nom de la connexion réseau actuelle.</span><span class="sxs-lookup"><span data-stu-id="d8262-212">Name of the current network connection.</span></span> <span data-ttu-id="d8262-213">Il s’agit de la combinaison des valeurs dans **nom_distant** et **LocalName**.</span><span class="sxs-lookup"><span data-stu-id="d8262-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="d8262-214">Exemple : « \\ \\ NTRELEASE (c : \\ public) »</span><span class="sxs-lookup"><span data-stu-id="d8262-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="d8262-215">**Persistent**</span><span class="sxs-lookup"><span data-stu-id="d8262-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d8262-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-218">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Windows Networking Functions \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)»)</span><span class="sxs-lookup"><span data-stu-id="d8262-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-219">La connexion sera reconnectée automatiquement par le système d’exploitation lors de la prochaine ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="d8262-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="d8262-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d8262-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-223">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")</span><span class="sxs-lookup"><span data-stu-id="d8262-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-224">Nom du fournisseur propriétaire de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d8262-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="d8262-225">Cette propriété peut avoir la **valeur null** si le nom du fournisseur est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d8262-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d8262-226">**RemoteName**</span><span class="sxs-lookup"><span data-stu-id="d8262-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-229">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="d8262-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-230">Nom de ressource réseau distant pour une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="d8262-231">Pour une connexion active ou persistante, **nom_distant** contient le nom réseau associé au nom de la valeur dans la propriété **LocalName** .</span><span class="sxs-lookup"><span data-stu-id="d8262-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="d8262-232">Le nom dans **nom_distant** doit respecter les conventions d’affectation de noms du fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="d8262-233">Exemple : « \\ \\ NTRELEASE »</span><span class="sxs-lookup"><span data-stu-id="d8262-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="d8262-234">**RemovePath**</span><span class="sxs-lookup"><span data-stu-id="d8262-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-237">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")</span><span class="sxs-lookup"><span data-stu-id="d8262-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-238">Chemin d’accès complet à la ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-238">Full path to the network resource.</span></span>

<span data-ttu-id="d8262-239">Exemple : « \\ \\ infosrv1 \\ public »</span><span class="sxs-lookup"><span data-stu-id="d8262-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="d8262-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d8262-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-241">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-243">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Windows Networking structures \| [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")</span><span class="sxs-lookup"><span data-stu-id="d8262-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-244">Type de ressource à énumérer ou à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d8262-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="d8262-245">**Disque** (« Disk »)</span><span class="sxs-lookup"><span data-stu-id="d8262-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="d8262-246">**Imprimer** (« imprimer »)</span><span class="sxs-lookup"><span data-stu-id="d8262-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="d8262-247">**Any** (« any »)</span><span class="sxs-lookup"><span data-stu-id="d8262-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-248">**État**</span><span class="sxs-lookup"><span data-stu-id="d8262-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-251">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d8262-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-252">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d8262-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="d8262-253">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="d8262-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d8262-254">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="d8262-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d8262-255">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="d8262-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d8262-256">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d8262-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d8262-257">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d8262-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d8262-258">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d8262-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d8262-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8262-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d8262-260">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8262-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d8262-261">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d8262-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d8262-262">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d8262-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d8262-263">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d8262-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8262-264">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d8262-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d8262-265">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d8262-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d8262-266">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d8262-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d8262-267">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d8262-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d8262-268">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d8262-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d8262-269">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d8262-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d8262-270">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d8262-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d8262-271">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d8262-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d8262-272">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d8262-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d8262-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d8262-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8262-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d8262-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8262-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d8262-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8262-276">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Windows Networking Functions \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)»)</span><span class="sxs-lookup"><span data-stu-id="d8262-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="d8262-277">Nom d’utilisateur ou nom d’utilisateur par défaut utilisé pour établir une connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="d8262-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="d8262-278">Exemple : « système »</span><span class="sxs-lookup"><span data-stu-id="d8262-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8262-279">Notes</span><span class="sxs-lookup"><span data-stu-id="d8262-279">Remarks</span></span>

<span data-ttu-id="d8262-280">La classe **Win32 \_ NetworkConnection** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d8262-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8262-281">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8262-281">Examples</span></span>

<span data-ttu-id="d8262-282">L’exemple de code VBScript suivant récupère des informations sur la connexion au réseau local.</span><span class="sxs-lookup"><span data-stu-id="d8262-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="d8262-283">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8262-283">Requirements</span></span>



| <span data-ttu-id="d8262-284">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8262-284">Requirement</span></span> | <span data-ttu-id="d8262-285">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8262-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8262-286">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8262-286">Minimum supported client</span></span><br/> | <span data-ttu-id="d8262-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8262-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8262-288">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8262-288">Minimum supported server</span></span><br/> | <span data-ttu-id="d8262-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8262-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8262-290">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8262-290">Namespace</span></span><br/>                | <span data-ttu-id="d8262-291">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d8262-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8262-292">MOF</span><span class="sxs-lookup"><span data-stu-id="d8262-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8262-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8262-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8262-294">DLL</span><span class="sxs-lookup"><span data-stu-id="d8262-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8262-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8262-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8262-296">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8262-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8262-297">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d8262-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d8262-298">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d8262-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
