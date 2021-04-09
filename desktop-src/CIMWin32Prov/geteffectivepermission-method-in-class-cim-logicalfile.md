---
description: Détermine si l’appelant a les autorisations agrégées sur l' \_ objet CIM LogicalFile et le partage sur lequel le fichier ou le répertoire réside, comme spécifié par l’argument d’autorisation.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Méthode GetEffectivePermission de la classe CIM_LogicalFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110499"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="71ac7-103">Méthode GetEffectivePermission de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="71ac7-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="71ac7-104">La méthode **GetEffectivePermission** détermine si l’appelant dispose des autorisations agrégées sur l' [**objet \_ LogicalFile CIM**](cim-logicalfile.md) et du partage sur lequel le fichier ou le répertoire réside, comme spécifié par l’argument *permissions* .</span><span class="sxs-lookup"><span data-stu-id="71ac7-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71ac7-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="71ac7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="71ac7-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="71ac7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="71ac7-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="71ac7-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="71ac7-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="71ac7-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="71ac7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71ac7-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="71ac7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71ac7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ac7-111">*Autorisations* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="71ac7-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ac7-112">Liste des autorisations à propos desquelles l’utilisateur peut se renseigner.</span><span class="sxs-lookup"><span data-stu-id="71ac7-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="71ac7-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Fichier \_ LIRE les \_ données (fichier) ou \_ \_ Répertoire de liste de fichiers (répertoire)** (1)</span><span class="sxs-lookup"><span data-stu-id="71ac7-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-114">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="71ac7-115">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="71ac7-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="71ac7-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Fichier \_ ÉCRIRE des \_ données (fichier) ou \_ Ajouter un fichier \_ (répertoire)** (2)</span><span class="sxs-lookup"><span data-stu-id="71ac7-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-117">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="71ac7-118">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="71ac7-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="71ac7-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Fichier \_ Ajouter des \_ données (fichier) ou un fichier \_ Ajouter un \_ sous-répertoire (répertoire)** (4)</span><span class="sxs-lookup"><span data-stu-id="71ac7-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-120">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="71ac7-121">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="71ac7-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="71ac7-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Fichier \_ LIRE \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="71ac7-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-123">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="71ac7-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="71ac7-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Fichier \_ ÉCRIRE \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="71ac7-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-125">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="71ac7-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="71ac7-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Fichier \_ EXECUTe (file) ou FILE \_ Traversal (Directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="71ac7-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-127">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-127">Grants the right to execute a file.</span></span> <span data-ttu-id="71ac7-128">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="71ac7-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="71ac7-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Fichier \_ SUPPRIMER un \_ enfant (répertoire)** (64)</span><span class="sxs-lookup"><span data-stu-id="71ac7-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-130">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient, même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="71ac7-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="71ac7-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Fichier \_ \_Attributs de lecture** (128)</span><span class="sxs-lookup"><span data-stu-id="71ac7-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-132">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="71ac7-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Fichier \_ \_Attributs d’écriture** (256)</span><span class="sxs-lookup"><span data-stu-id="71ac7-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-134">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="71ac7-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="71ac7-135"><span id="DELETE"></span><span id="delete"></span>**Supprimer** (65536)</span><span class="sxs-lookup"><span data-stu-id="71ac7-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-136">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="71ac7-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="71ac7-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072)</span><span class="sxs-lookup"><span data-stu-id="71ac7-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-138">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="71ac7-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="71ac7-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="71ac7-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-140">Octroie l’accès en écriture à la liste de contrôle d’accès discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="71ac7-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="71ac7-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Écriture \_ PROPRIÉTAIRE** (524288)</span><span class="sxs-lookup"><span data-stu-id="71ac7-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-142">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="71ac7-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="71ac7-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchroniser** (1048576)</span><span class="sxs-lookup"><span data-stu-id="71ac7-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="71ac7-144">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="71ac7-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ac7-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71ac7-145">Return value</span></span>

<span data-ttu-id="71ac7-146">Retourne la **valeur true** si l’appel a l’autorisation nécessaire. Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="71ac7-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ac7-147">Notes</span><span class="sxs-lookup"><span data-stu-id="71ac7-147">Remarks</span></span>

<span data-ttu-id="71ac7-148">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="71ac7-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="71ac7-149">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="71ac7-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="71ac7-150">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="71ac7-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="71ac7-151">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="71ac7-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ac7-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71ac7-152">Requirements</span></span>



| <span data-ttu-id="71ac7-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71ac7-153">Requirement</span></span> | <span data-ttu-id="71ac7-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="71ac7-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ac7-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71ac7-155">Minimum supported client</span></span><br/> | <span data-ttu-id="71ac7-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71ac7-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71ac7-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71ac7-157">Minimum supported server</span></span><br/> | <span data-ttu-id="71ac7-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71ac7-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71ac7-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="71ac7-159">Namespace</span></span><br/>                | <span data-ttu-id="71ac7-160">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="71ac7-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71ac7-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="71ac7-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ac7-162"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ac7-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="71ac7-163">MOF</span><span class="sxs-lookup"><span data-stu-id="71ac7-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71ac7-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71ac7-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71ac7-165">DLL</span><span class="sxs-lookup"><span data-stu-id="71ac7-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71ac7-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ac7-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ac7-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71ac7-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ac7-168">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="71ac7-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="71ac7-169">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="71ac7-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

