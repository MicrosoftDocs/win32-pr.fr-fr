---
description: Modifie les autorisations de sécurité pour le fichier d’échange logique qui est spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861037"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="96329-103">Méthode ChangeSecurityPermissionsEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="96329-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="96329-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier de pagination logique qui est spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="96329-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="96329-105">Si le fichier logique est un répertoire, cette méthode est récursive et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="96329-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="96329-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="96329-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="96329-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="96329-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="96329-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96329-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="96329-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96329-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96329-110">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96329-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96329-111">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="96329-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="96329-112">Ce paramètre contient de nouvelles autorisations de sécurité pour l’instance du [**\_ fichier d’échange Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="96329-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="96329-113">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96329-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96329-114">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="96329-114">Security privilege to be modified.</span></span> <span data-ttu-id="96329-115">Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="96329-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="96329-116">-ou-</span><span class="sxs-lookup"><span data-stu-id="96329-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="96329-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="96329-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="96329-118">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="96329-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="96329-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="96329-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="96329-120">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="96329-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="96329-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="96329-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="96329-122">Modifiez la liste DACL du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="96329-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="96329-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="96329-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="96329-124">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="96329-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="96329-125">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96329-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96329-126">Nom du fichier ou du répertoire dans lequel la méthode **ChangeSecurityPermissionsEX** a échoué.</span><span class="sxs-lookup"><span data-stu-id="96329-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="96329-127">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="96329-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="96329-128">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="96329-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="96329-129">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **ChangeSecurityPermissionsEX**.</span><span class="sxs-lookup"><span data-stu-id="96329-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="96329-130">En général, le paramètre *StartFileName* est le paramètre *StartFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="96329-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="96329-131">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="96329-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="96329-132">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="96329-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="96329-133">Si la **valeur est true**, la modification de la propriété est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="96329-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="96329-134">Pour les instances de fichier, le paramètre *recursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="96329-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96329-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96329-135">Return value</span></span>

<span data-ttu-id="96329-136">Retourne la valeur 0 (zéro) si les autorisations sont modifiées et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="96329-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="96329-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="96329-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="96329-138">0</span><span class="sxs-lookup"><span data-stu-id="96329-138">0</span></span>

<span data-ttu-id="96329-139">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="96329-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="96329-140">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="96329-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="96329-141">2</span><span class="sxs-lookup"><span data-stu-id="96329-141">2</span></span>

<span data-ttu-id="96329-142">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="96329-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="96329-143">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="96329-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="96329-144">8</span><span class="sxs-lookup"><span data-stu-id="96329-144">8</span></span>

<span data-ttu-id="96329-145">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="96329-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="96329-146">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="96329-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="96329-147">9</span><span class="sxs-lookup"><span data-stu-id="96329-147">9</span></span>

<span data-ttu-id="96329-148">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="96329-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="96329-149">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="96329-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="96329-150">10</span><span class="sxs-lookup"><span data-stu-id="96329-150">10</span></span>

<span data-ttu-id="96329-151">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="96329-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="96329-152">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="96329-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="96329-153">11</span><span class="sxs-lookup"><span data-stu-id="96329-153">11</span></span>

<span data-ttu-id="96329-154">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="96329-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="96329-155">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="96329-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="96329-156">12</span><span class="sxs-lookup"><span data-stu-id="96329-156">12</span></span>

<span data-ttu-id="96329-157">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="96329-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="96329-158">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="96329-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="96329-159">13</span><span class="sxs-lookup"><span data-stu-id="96329-159">13</span></span>

<span data-ttu-id="96329-160">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="96329-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="96329-161">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="96329-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="96329-162">14</span><span class="sxs-lookup"><span data-stu-id="96329-162">14</span></span>

<span data-ttu-id="96329-163">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="96329-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="96329-164">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="96329-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="96329-165">15</span><span class="sxs-lookup"><span data-stu-id="96329-165">15</span></span>

<span data-ttu-id="96329-166">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="96329-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="96329-167">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="96329-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="96329-168">16</span><span class="sxs-lookup"><span data-stu-id="96329-168">16</span></span>

<span data-ttu-id="96329-169">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="96329-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="96329-170">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="96329-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="96329-171">17</span><span class="sxs-lookup"><span data-stu-id="96329-171">17</span></span>

<span data-ttu-id="96329-172">Un privilège requis pour l’opération est manquant.</span><span class="sxs-lookup"><span data-stu-id="96329-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="96329-173">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="96329-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="96329-174">21</span><span class="sxs-lookup"><span data-stu-id="96329-174">21</span></span>

<span data-ttu-id="96329-175">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="96329-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96329-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96329-176">Requirements</span></span>



| <span data-ttu-id="96329-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96329-177">Requirement</span></span> | <span data-ttu-id="96329-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="96329-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96329-179">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96329-179">Minimum supported client</span></span><br/> | <span data-ttu-id="96329-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96329-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96329-181">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96329-181">Minimum supported server</span></span><br/> | <span data-ttu-id="96329-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96329-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96329-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96329-183">Namespace</span></span><br/>                | <span data-ttu-id="96329-184">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="96329-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="96329-185">MOF</span><span class="sxs-lookup"><span data-stu-id="96329-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96329-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96329-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="96329-187">DLL</span><span class="sxs-lookup"><span data-stu-id="96329-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96329-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96329-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96329-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96329-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="96329-190">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="96329-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="96329-191">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="96329-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

