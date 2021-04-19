---
description: Les classes WMI qui représentent des fichiers ou des répertoires, tels que Win32 \_ CodecFile ou \_ un fichier de fichier CIM, contiennent une propriété AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de droits d’accès aux fichiers et aux répertoires (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545901"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="c51da-103">Constantes de droits d’accès aux fichiers et aux répertoires</span><span class="sxs-lookup"><span data-stu-id="c51da-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="c51da-104">Les classes WMI qui représentent des fichiers ou des répertoires, tels que [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) ou un [**fichier de \_ fichier CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), contiennent une propriété **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="c51da-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="c51da-105">Cette propriété contient des paramètres de bits qui spécifient les droits d’accès qu’un utilisateur ou un groupe doit avoir pour un accès ou des opérations spécifiques sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="c51da-106">Pour plus d’informations, consultez [sécurité des fichiers et droits d’accès](/windows/desktop/FileIO/file-security-and-access-rights) et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c51da-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="c51da-107">Les classes de fichiers ou de répertoires qui contiennent une propriété **AccessMask** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c51da-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="c51da-108">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="c51da-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="c51da-109">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="c51da-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="c51da-110">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c51da-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="c51da-111">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="c51da-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="c51da-112">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="c51da-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="c51da-113">[**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c51da-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="c51da-114">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="c51da-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="c51da-115">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="c51da-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="c51da-116">La liste suivante répertorie les valeurs des droits d’accès aux fichiers et aux répertoires dans la propriété **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="c51da-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="c51da-117">Cette propriété est une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="c51da-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="c51da-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_lire les \_ données de fichier**</span><span class="sxs-lookup"><span data-stu-id="c51da-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c51da-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-120">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_Répertoire de liste de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c51da-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-123">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="c51da-124">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="c51da-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_données d’écriture de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-126">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="c51da-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-127">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**fichier \_ ajouter \_ un fichier**</span><span class="sxs-lookup"><span data-stu-id="c51da-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-129">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="c51da-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-130">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="c51da-131">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="c51da-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FICHIER \_ Ajouter des \_ données**</span><span class="sxs-lookup"><span data-stu-id="c51da-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c51da-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-134">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="c51da-135">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="c51da-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FICHIER \_ Ajouter un \_ sous-répertoire**</span><span class="sxs-lookup"><span data-stu-id="c51da-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="c51da-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-138">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="c51da-139">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="c51da-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**lecture de fichier \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="c51da-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="c51da-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-142">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="c51da-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**écriture de fichier \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="c51da-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="c51da-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-145">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="c51da-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**exécution du fichier \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c51da-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-148">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**parcours de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="c51da-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-151">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-151">Grants the right to execute a file.</span></span> <span data-ttu-id="c51da-152">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="c51da-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_supprimer un \_ enfant de fichier**</span><span class="sxs-lookup"><span data-stu-id="c51da-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="c51da-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-155">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c51da-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_attributs de lecture de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="c51da-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-158">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_attributs d’écriture de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="c51da-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-161">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="c51da-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-162"><span id="DELETE"></span><span id="delete"></span>**SUPPRIMER**</span><span class="sxs-lookup"><span data-stu-id="c51da-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="c51da-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-164">Accorde le droit de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="c51da-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**LIRE \_ le contrôle**</span><span class="sxs-lookup"><span data-stu-id="c51da-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="c51da-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-167">Accorde le droit de lire les informations du descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="c51da-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**ÉCRITURE \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="c51da-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="c51da-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-170">Accorde le droit de modifier la liste DACL dans le descripteur de sécurité de l’objet pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="c51da-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**propriétaire en écriture \_**</span><span class="sxs-lookup"><span data-stu-id="c51da-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="c51da-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-173">Accorde le droit de modifier le propriétaire dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c51da-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c51da-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**NON**</span><span class="sxs-lookup"><span data-stu-id="c51da-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c51da-175">1048576 ()</span><span class="sxs-lookup"><span data-stu-id="c51da-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="c51da-176">Accorde le droit d’utiliser l’objet pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c51da-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="c51da-177">Cela permet à un processus d’attendre jusqu’à ce que l’objet soit dans un état signalé.</span><span class="sxs-lookup"><span data-stu-id="c51da-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="c51da-178">Certains types d’objets ne prennent pas en charge ce droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="c51da-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c51da-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c51da-179">Requirements</span></span>



| <span data-ttu-id="c51da-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c51da-180">Requirement</span></span> | <span data-ttu-id="c51da-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="c51da-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c51da-182">En-tête</span><span class="sxs-lookup"><span data-stu-id="c51da-182">Header</span></span><br/> | <dl> <span data-ttu-id="c51da-183"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51da-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c51da-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c51da-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51da-185">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="c51da-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="c51da-186">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="c51da-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

