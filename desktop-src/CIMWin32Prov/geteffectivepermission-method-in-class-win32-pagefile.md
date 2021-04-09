---
description: Détermine si l’utilisateur dispose de toutes les autorisations requises spécifiées dans le paramètre des autorisations identifié pour l' \_ objet pagefile Win32, le répertoire et le partage où se trouve le fichier d’échange, si le fichier ou le répertoire se trouve sur un partage.
ms.assetid: 1c417ac2-6968-4faf-b596-8df9308f8647
ms.tgt_platform: multiple
title: Méthode GetEffectivePermission de la classe Win32_PageFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3b9985d18e93f3a3dbcc8f65484bf3fd72284fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950556"
---
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a><span data-ttu-id="9d31a-103">Méthode GetEffectivePermission de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="9d31a-103">GetEffectivePermission method of the Win32\_PageFile class</span></span>

<span data-ttu-id="9d31a-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) détermine si l’utilisateur dispose de toutes les autorisations requises spécifiées dans le paramètre des *autorisations* identifié pour l’objet [**\_ pagefile Win32**](win32-pagefile.md) , le répertoire et le partage où se trouve le fichier d’échange, si le fichier ou le répertoire se trouve sur un partage.</span><span class="sxs-lookup"><span data-stu-id="9d31a-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter identified for the [**Win32\_PageFile**](win32-pagefile.md) object, directory, and share where the paging file is located, if the file or directory are on a share.</span></span>

<span data-ttu-id="9d31a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9d31a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9d31a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9d31a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d31a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d31a-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="9d31a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d31a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d31a-109">*Autorisations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d31a-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d31a-110">Bitmap des autorisations à propos desquelles l’appelant peut se renseigner.</span><span class="sxs-lookup"><span data-stu-id="9d31a-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="9d31a-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ fichiers de données (fichier) \_ \_ Répertoire de la liste de fichiers (répertoire)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9d31a-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-112">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="9d31a-113">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="9d31a-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="9d31a-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE le fichier de \_ données (fichier) ajouter un fichier \_ \_ (répertoire)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="9d31a-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-115">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="9d31a-116">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="9d31a-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="9d31a-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Fichier \_ \_Ajouter un fichier de données (fichier) \_ Ajouter un \_ sous-répertoire (répertoire)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="9d31a-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-118">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="9d31a-119">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="9d31a-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="9d31a-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ READ \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="9d31a-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-121">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="9d31a-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="9d31a-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="9d31a-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-123">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="9d31a-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="9d31a-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Fichier \_ EXÉCUTER (fichier) parcourir un fichier \_ (répertoire)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="9d31a-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-125">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-125">Grants the right to execute a file.</span></span> <span data-ttu-id="9d31a-126">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="9d31a-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="9d31a-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="9d31a-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-128">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient, même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9d31a-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="9d31a-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="9d31a-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-130">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="9d31a-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="9d31a-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-132">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="9d31a-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="9d31a-133"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="9d31a-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-134">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="9d31a-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="9d31a-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9d31a-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-136">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9d31a-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="9d31a-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="9d31a-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-138">Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="9d31a-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="9d31a-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="9d31a-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-140">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="9d31a-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="9d31a-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisation** (1048576)</span><span class="sxs-lookup"><span data-stu-id="9d31a-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="9d31a-142">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="9d31a-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d31a-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d31a-143">Return value</span></span>

<span data-ttu-id="9d31a-144">Retourne la **valeur true** si l’appelant a les autorisations spécifiées et **false** si l’appelant n’a pas les autorisations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9d31a-144">Returns **True** if the caller has the specified permissions, and **false** if the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d31a-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d31a-145">Requirements</span></span>



| <span data-ttu-id="9d31a-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d31a-146">Requirement</span></span> | <span data-ttu-id="9d31a-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d31a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d31a-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d31a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9d31a-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d31a-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d31a-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d31a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9d31a-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d31a-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d31a-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9d31a-152">Namespace</span></span><br/>                | <span data-ttu-id="9d31a-153">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9d31a-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d31a-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d31a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d31a-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d31a-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="9d31a-156">MOF</span><span class="sxs-lookup"><span data-stu-id="9d31a-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d31a-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d31a-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d31a-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9d31a-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d31a-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d31a-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d31a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d31a-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="9d31a-161">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d31a-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9d31a-162">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="9d31a-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

