---
description: Modifie les autorisations de sécurité pour le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200967"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="6a522-103">Méthode ChangeSecurityPermissionsEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="6a522-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="6a522-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="6a522-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="6a522-105">Si le fichier logique est un répertoire, cette méthode est récursive et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="6a522-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="6a522-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a522-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a522-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a522-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a522-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a522-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6a522-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a522-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a522-110">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a522-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a522-111">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6a522-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="6a522-112">Ce paramètre contient de nouvelles autorisations de sécurité pour l’instance du [**\_ fichier d’échange Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="6a522-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a522-113">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a522-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a522-114">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="6a522-114">Security privilege to be modified.</span></span> <span data-ttu-id="6a522-115">Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6a522-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="6a522-116">-ou-</span><span class="sxs-lookup"><span data-stu-id="6a522-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6a522-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="6a522-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a522-118">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6a522-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6a522-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="6a522-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a522-120">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6a522-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6a522-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="6a522-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a522-122">Modifiez la liste DACL du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6a522-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6a522-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="6a522-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a522-124">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6a522-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a522-125">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a522-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a522-126">Nom du fichier ou du répertoire dans lequel la méthode **ChangeSecurityPermissionsEX** a échoué.</span><span class="sxs-lookup"><span data-stu-id="6a522-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="6a522-127">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="6a522-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-128">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6a522-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a522-129">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **ChangeSecurityPermissionsEX**.</span><span class="sxs-lookup"><span data-stu-id="6a522-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="6a522-130">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="6a522-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="6a522-131">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="6a522-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="6a522-132">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6a522-132">This parameter is optional.</span></span>

<span data-ttu-id="6a522-133">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="6a522-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-134">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6a522-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a522-135">Si la **valeur est true**, la modification de la propriété est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="6a522-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="6a522-136">Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6a522-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="6a522-137">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6a522-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a522-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a522-138">Return value</span></span>

<span data-ttu-id="6a522-139">Retourne la valeur 0 (zéro) si les autorisations sont modifiées et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="6a522-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a522-140">**Success**</span><span class="sxs-lookup"><span data-stu-id="6a522-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-141">0</span><span class="sxs-lookup"><span data-stu-id="6a522-141">0</span></span>

<span data-ttu-id="6a522-142">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="6a522-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-143">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="6a522-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-144">2</span><span class="sxs-lookup"><span data-stu-id="6a522-144">2</span></span>

<span data-ttu-id="6a522-145">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="6a522-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-146">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="6a522-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-147">8</span><span class="sxs-lookup"><span data-stu-id="6a522-147">8</span></span>

<span data-ttu-id="6a522-148">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6a522-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-149">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="6a522-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-150">9</span><span class="sxs-lookup"><span data-stu-id="6a522-150">9</span></span>

<span data-ttu-id="6a522-151">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a522-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-152">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="6a522-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-153">10</span><span class="sxs-lookup"><span data-stu-id="6a522-153">10</span></span>

<span data-ttu-id="6a522-154">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6a522-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-155">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="6a522-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-156">11</span><span class="sxs-lookup"><span data-stu-id="6a522-156">11</span></span>

<span data-ttu-id="6a522-157">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="6a522-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-158">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6a522-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-159">12</span><span class="sxs-lookup"><span data-stu-id="6a522-159">12</span></span>

<span data-ttu-id="6a522-160">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="6a522-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-161">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="6a522-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-162">13</span><span class="sxs-lookup"><span data-stu-id="6a522-162">13</span></span>

<span data-ttu-id="6a522-163">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="6a522-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-164">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="6a522-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-165">14</span><span class="sxs-lookup"><span data-stu-id="6a522-165">14</span></span>

<span data-ttu-id="6a522-166">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6a522-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-167">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="6a522-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-168">15</span><span class="sxs-lookup"><span data-stu-id="6a522-168">15</span></span>

<span data-ttu-id="6a522-169">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="6a522-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-170">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="6a522-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-171">16</span><span class="sxs-lookup"><span data-stu-id="6a522-171">16</span></span>

<span data-ttu-id="6a522-172">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a522-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-173">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="6a522-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-174">17</span><span class="sxs-lookup"><span data-stu-id="6a522-174">17</span></span>

<span data-ttu-id="6a522-175">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="6a522-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6a522-176">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="6a522-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6a522-177">21</span><span class="sxs-lookup"><span data-stu-id="6a522-177">21</span></span>

<span data-ttu-id="6a522-178">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a522-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a522-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a522-179">Requirements</span></span>



| <span data-ttu-id="6a522-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a522-180">Requirement</span></span> | <span data-ttu-id="6a522-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a522-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a522-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a522-182">Minimum supported client</span></span><br/> | <span data-ttu-id="6a522-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a522-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a522-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a522-184">Minimum supported server</span></span><br/> | <span data-ttu-id="6a522-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a522-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a522-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a522-186">Namespace</span></span><br/>                | <span data-ttu-id="6a522-187">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6a522-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a522-188">MOF</span><span class="sxs-lookup"><span data-stu-id="6a522-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a522-189"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a522-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a522-190">DLL</span><span class="sxs-lookup"><span data-stu-id="6a522-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a522-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a522-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a522-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a522-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a522-193">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a522-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a522-194">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="6a522-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

