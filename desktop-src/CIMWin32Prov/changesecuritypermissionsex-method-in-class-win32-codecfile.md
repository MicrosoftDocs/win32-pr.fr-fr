---
description: Modifie les autorisations de sécurité pour le fichier de codec spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861038"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="3c26b-103">Méthode ChangeSecurityPermissionsEx de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="3c26b-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="3c26b-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier de codec spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="3c26b-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="3c26b-105">Si le fichier logique est un répertoire, cette méthode est récursive et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="3c26b-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="3c26b-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3c26b-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3c26b-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3c26b-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c26b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c26b-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3c26b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c26b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c26b-110">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c26b-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-111">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3c26b-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="3c26b-112">Ce descripteur contient de nouvelles autorisations de sécurité pour l’instance de [**Win32 \_ CodecFile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="3c26b-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-113">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c26b-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-114">Privilège de sécurité réel à modifier.</span><span class="sxs-lookup"><span data-stu-id="3c26b-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="3c26b-115">Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3c26b-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="3c26b-116">-ou-</span><span class="sxs-lookup"><span data-stu-id="3c26b-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3c26b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3c26b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3c26b-118">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3c26b-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3c26b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ GROUPEr les \_ \_ informations de sécurité** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="3c26b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="3c26b-120">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3c26b-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3c26b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="3c26b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="3c26b-122">Modifiez la liste de contrôle d’accès discrétionnaire (DACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3c26b-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3c26b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="3c26b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="3c26b-124">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="3c26b-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3c26b-125">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c26b-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-126">Nom du fichier ou du répertoire dans lequel la méthode **ChangeSecurityPermissionsEX** a échoué.</span><span class="sxs-lookup"><span data-stu-id="3c26b-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="3c26b-127">Ce paramètre est NULL lorsque la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="3c26b-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-128">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3c26b-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-129">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **ChangeSecurityPermissionsEX**.</span><span class="sxs-lookup"><span data-stu-id="3c26b-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="3c26b-130">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="3c26b-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="3c26b-131">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="3c26b-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-132">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3c26b-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-133">Si la **valeur est true**, les modifications de propriété sont appliquées de manière récursive aux fichiers et répertoires du répertoire que l’instance [**\_ LogicalFile CIM**](cim-logicalfile.md) spécifie.</span><span class="sxs-lookup"><span data-stu-id="3c26b-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="3c26b-134">Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3c26b-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c26b-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c26b-135">Return value</span></span>

<span data-ttu-id="3c26b-136">Retourne une valeur 0 (zéro) si les autorisations sont modifiées et un nombre différent pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3c26b-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3c26b-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="3c26b-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-138">0</span><span class="sxs-lookup"><span data-stu-id="3c26b-138">0</span></span>

<span data-ttu-id="3c26b-139">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="3c26b-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-140">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="3c26b-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-141">2</span><span class="sxs-lookup"><span data-stu-id="3c26b-141">2</span></span>

<span data-ttu-id="3c26b-142">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="3c26b-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-143">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="3c26b-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-144">8</span><span class="sxs-lookup"><span data-stu-id="3c26b-144">8</span></span>

<span data-ttu-id="3c26b-145">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3c26b-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-146">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="3c26b-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-147">9</span><span class="sxs-lookup"><span data-stu-id="3c26b-147">9</span></span>

<span data-ttu-id="3c26b-148">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3c26b-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-149">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="3c26b-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-150">10</span><span class="sxs-lookup"><span data-stu-id="3c26b-150">10</span></span>

<span data-ttu-id="3c26b-151">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3c26b-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-152">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="3c26b-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-153">11</span><span class="sxs-lookup"><span data-stu-id="3c26b-153">11</span></span>

<span data-ttu-id="3c26b-154">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="3c26b-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-155">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3c26b-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-156">12</span><span class="sxs-lookup"><span data-stu-id="3c26b-156">12</span></span>

<span data-ttu-id="3c26b-157">La plateforme n’est pas Windows NT ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3c26b-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-158">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="3c26b-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-159">13</span><span class="sxs-lookup"><span data-stu-id="3c26b-159">13</span></span>

<span data-ttu-id="3c26b-160">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="3c26b-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-161">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="3c26b-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-162">14</span><span class="sxs-lookup"><span data-stu-id="3c26b-162">14</span></span>

<span data-ttu-id="3c26b-163">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="3c26b-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-164">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="3c26b-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-165">15</span><span class="sxs-lookup"><span data-stu-id="3c26b-165">15</span></span>

<span data-ttu-id="3c26b-166">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="3c26b-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-167">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="3c26b-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-168">16</span><span class="sxs-lookup"><span data-stu-id="3c26b-168">16</span></span>

<span data-ttu-id="3c26b-169">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3c26b-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-170">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="3c26b-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-171">17</span><span class="sxs-lookup"><span data-stu-id="3c26b-171">17</span></span>

<span data-ttu-id="3c26b-172">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="3c26b-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3c26b-173">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="3c26b-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3c26b-174">21</span><span class="sxs-lookup"><span data-stu-id="3c26b-174">21</span></span>

<span data-ttu-id="3c26b-175">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3c26b-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c26b-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c26b-176">Requirements</span></span>



| <span data-ttu-id="3c26b-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c26b-177">Requirement</span></span> | <span data-ttu-id="3c26b-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c26b-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c26b-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c26b-179">Minimum supported client</span></span><br/> | <span data-ttu-id="3c26b-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c26b-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c26b-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c26b-181">Minimum supported server</span></span><br/> | <span data-ttu-id="3c26b-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c26b-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c26b-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c26b-183">Namespace</span></span><br/>                | <span data-ttu-id="3c26b-184">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3c26b-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c26b-185">MOF</span><span class="sxs-lookup"><span data-stu-id="3c26b-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c26b-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c26b-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c26b-187">DLL</span><span class="sxs-lookup"><span data-stu-id="3c26b-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c26b-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c26b-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c26b-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c26b-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c26b-190">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c26b-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3c26b-191">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="3c26b-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

