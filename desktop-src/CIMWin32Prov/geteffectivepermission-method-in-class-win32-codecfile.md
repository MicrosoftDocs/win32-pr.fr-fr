---
description: Utilise les valeurs définies dans le paramètre permissions pour déterminer si l’utilisateur dispose des autorisations spécifiées dans la propriété AccessMask de l' \_ objet Win32 CodecFile qui représente le fichier de codec.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: Méthode GetEffectivePermission de la classe Win32_CodecFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860949"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="ab3a1-103">Méthode GetEffectivePermission de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="ab3a1-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="ab3a1-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) utilise les valeurs définies dans le paramètre *permissions* pour déterminer si l’utilisateur dispose des autorisations spécifiées dans la propriété **AccessMask** de l’objet [**Win32 \_ CodecFile**](win32-codecfile.md) qui représente le fichier de codec.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="ab3a1-105">Les autorisations s’appliquent au fichier, au répertoire dans lequel le fichier réside et au partage, si le répertoire ou le fichier se trouve dans un partage.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="ab3a1-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ab3a1-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ab3a1-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ab3a1-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3a1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab3a1-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="ab3a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab3a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab3a1-110">*Autorisations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab3a1-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab3a1-111">Bitmap des autorisations définies dans la propriété **AccessMask** de l’objet [**Win32 \_ CodecFile**](win32-codecfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ab3a1-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ab3a1-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ fichiers de données (fichier) \_ \_ Répertoire de la liste de fichiers (répertoire)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-113">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="ab3a1-114">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="ab3a1-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE le fichier de \_ données (fichier) ajouter un fichier \_ \_ (répertoire)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-116">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="ab3a1-117">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="ab3a1-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Fichier \_ \_Ajouter un fichier de données (fichier) \_ Ajouter un \_ sous-répertoire (répertoire)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-119">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="ab3a1-120">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="ab3a1-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ READ \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-122">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="ab3a1-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-124">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="ab3a1-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXÉCUTER (fichier) parcourir un fichier \_ (répertoire)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-126">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-126">Grants the right to execute a file.</span></span> <span data-ttu-id="ab3a1-127">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="ab3a1-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-129">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient, même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="ab3a1-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-131">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="ab3a1-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-133">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="ab3a1-134"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-135">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="ab3a1-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-137">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="ab3a1-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-139">Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (ACL).</span><span class="sxs-lookup"><span data-stu-id="ab3a1-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="ab3a1-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-141">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="ab3a1-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisation** (1048576)</span><span class="sxs-lookup"><span data-stu-id="ab3a1-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="ab3a1-143">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab3a1-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab3a1-144">Return value</span></span>

<span data-ttu-id="ab3a1-145">Retourne la **valeur true** lorsque l’appelant a les autorisations spécifiées, et **false** lorsque l’appelant n’a pas les autorisations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ab3a1-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3a1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab3a1-146">Requirements</span></span>



| <span data-ttu-id="ab3a1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab3a1-147">Requirement</span></span> | <span data-ttu-id="ab3a1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab3a1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3a1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab3a1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ab3a1-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab3a1-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab3a1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab3a1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ab3a1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab3a1-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab3a1-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ab3a1-153">Namespace</span></span><br/>                | <span data-ttu-id="ab3a1-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ab3a1-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab3a1-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab3a1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab3a1-156"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab3a1-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab3a1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ab3a1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab3a1-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab3a1-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab3a1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="ab3a1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab3a1-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab3a1-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab3a1-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab3a1-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab3a1-162">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab3a1-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ab3a1-163">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="ab3a1-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

