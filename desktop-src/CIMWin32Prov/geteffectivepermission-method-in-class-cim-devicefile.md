---
description: Détermine si l’appelant a les autorisations agrégées sur l' \_ objet CIM DeviceFile et le partage sur lequel le fichier ou le répertoire réside, comme spécifié par l’argument d’autorisation.
ms.assetid: e566f1f6-773e-4ecb-8145-369afaad0f99
ms.tgt_platform: multiple
title: Méthode GetEffectivePermission de la classe CIM_DeviceFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b74c489c41b3da83f0e009526af225fd7de889
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110503"
---
# <a name="geteffectivepermission-method-of-the-cim_devicefile-class"></a><span data-ttu-id="315aa-103">Méthode GetEffectivePermission de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="315aa-103">GetEffectivePermission method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="315aa-104">La méthode **GetEffectivePermission** détermine si l’appelant a les autorisations agrégées sur l' [**objet \_ DeviceFile CIM**](cim-devicefile.md) et le partage sur lequel le fichier ou le répertoire réside, comme spécifié par l’argument d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="315aa-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_DeviceFile**](cim-devicefile.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="315aa-105">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="315aa-105">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="315aa-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="315aa-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="315aa-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="315aa-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="315aa-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="315aa-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="315aa-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="315aa-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="315aa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="315aa-110">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="315aa-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="315aa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315aa-112">*Autorisations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="315aa-112">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315aa-113">Liste des autorisations sur lesquelles l’appelant peut se renseigner.</span><span class="sxs-lookup"><span data-stu-id="315aa-113">List of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="315aa-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ fichiers de données (fichier) \_ \_ Répertoire de la liste de fichiers (répertoire)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="315aa-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-115">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-115">Grants the right to read data from the file.</span></span> <span data-ttu-id="315aa-116">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="315aa-116">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="315aa-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE le fichier de \_ données (fichier) ajouter un fichier \_ \_ (répertoire)** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="315aa-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-118">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="315aa-119">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="315aa-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="315aa-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Fichier \_ \_Ajouter un fichier de données (fichier) \_ Ajouter un \_ sous-répertoire (répertoire)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="315aa-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-121">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-121">Grants the right to append data to the file.</span></span> <span data-ttu-id="315aa-122">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="315aa-122">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="315aa-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ READ \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="315aa-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-124">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="315aa-124">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="315aa-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="315aa-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-126">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="315aa-126">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="315aa-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Fichier \_ EXÉCUTER (fichier) parcourir un fichier \_ (répertoire)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="315aa-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-128">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-128">Grants the right to execute a file.</span></span> <span data-ttu-id="315aa-129">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="315aa-129">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="315aa-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="315aa-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-131">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient, même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="315aa-131">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="315aa-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="315aa-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-133">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-133">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="315aa-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="315aa-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-135">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="315aa-135">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="315aa-136"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="315aa-136"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-137">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="315aa-137">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="315aa-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="315aa-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-139">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="315aa-139">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="315aa-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="315aa-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-141">Octroie l’accès en écriture à la liste de contrôle d’accès discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="315aa-141">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="315aa-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="315aa-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-143">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="315aa-143">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="315aa-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisation** (1048576)</span><span class="sxs-lookup"><span data-stu-id="315aa-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="315aa-145">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="315aa-145">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315aa-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="315aa-146">Return value</span></span>

<span data-ttu-id="315aa-147">Retourne la **valeur true** si l’appel a l’autorisation nécessaire. Sinon, elle retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="315aa-147">Returns **True** if the call has the necessary permission; otherwise, it returns **True**.</span></span>

## <a name="remarks"></a><span data-ttu-id="315aa-148">Notes</span><span class="sxs-lookup"><span data-stu-id="315aa-148">Remarks</span></span>

<span data-ttu-id="315aa-149">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="315aa-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="315aa-150">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="315aa-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="315aa-151">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="315aa-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="315aa-152">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="315aa-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="315aa-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="315aa-153">Requirements</span></span>



| <span data-ttu-id="315aa-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="315aa-154">Requirement</span></span> | <span data-ttu-id="315aa-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="315aa-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="315aa-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="315aa-156">Minimum supported client</span></span><br/> | <span data-ttu-id="315aa-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="315aa-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="315aa-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="315aa-158">Minimum supported server</span></span><br/> | <span data-ttu-id="315aa-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="315aa-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="315aa-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="315aa-160">Namespace</span></span><br/>                | <span data-ttu-id="315aa-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="315aa-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="315aa-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="315aa-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="315aa-163"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="315aa-163"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="315aa-164">MOF</span><span class="sxs-lookup"><span data-stu-id="315aa-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="315aa-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="315aa-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="315aa-166">DLL</span><span class="sxs-lookup"><span data-stu-id="315aa-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="315aa-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315aa-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315aa-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="315aa-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315aa-169">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="315aa-169">**CIM\_DeviceFile**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="315aa-170">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="315aa-170">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

