---
description: Modifie les autorisations de sécurité pour le fichier de raccourci logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483504"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="02353-103">Méthode ChangeSecurityPermissions de la \_ classe Win32 ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="02353-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="02353-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de raccourci logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="02353-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="02353-105">Si le fichier logique est un répertoire, **ChangeSecurityPermissions** est récursif et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="02353-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="02353-106">**ChangeSecurityPermissions** retourne une valeur entière égale à 0 (zéro) si les autorisations sont modifiées, et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="02353-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="02353-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="02353-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="02353-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="02353-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="02353-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02353-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="02353-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02353-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02353-111">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02353-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02353-112">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="02353-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="02353-113">Ce descripteur contient de nouvelles autorisations de sécurité pour l’instance du [**\_ fichier d’échange Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="02353-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="02353-114">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02353-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02353-115">Privilège de sécurité réel à modifier.</span><span class="sxs-lookup"><span data-stu-id="02353-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="02353-116">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="02353-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="02353-117">ou</span><span class="sxs-lookup"><span data-stu-id="02353-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="02353-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="02353-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="02353-119">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="02353-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="02353-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="02353-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="02353-121">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="02353-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="02353-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="02353-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="02353-123">Modifiez la liste de contrôle d’accès discrétionnaire (DACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="02353-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="02353-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="02353-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="02353-125">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="02353-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02353-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02353-126">Return value</span></span>

<span data-ttu-id="02353-127">Retourne la valeur 0 (zéro) si les autorisations sont modifiées et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="02353-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="02353-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="02353-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="02353-129">0</span><span class="sxs-lookup"><span data-stu-id="02353-129">0</span></span>

<span data-ttu-id="02353-130">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="02353-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="02353-131">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="02353-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="02353-132">2</span><span class="sxs-lookup"><span data-stu-id="02353-132">2</span></span>

<span data-ttu-id="02353-133">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="02353-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="02353-134">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="02353-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="02353-135">8</span><span class="sxs-lookup"><span data-stu-id="02353-135">8</span></span>

<span data-ttu-id="02353-136">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="02353-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="02353-137">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="02353-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="02353-138">9</span><span class="sxs-lookup"><span data-stu-id="02353-138">9</span></span>

<span data-ttu-id="02353-139">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02353-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="02353-140">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="02353-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="02353-141">10</span><span class="sxs-lookup"><span data-stu-id="02353-141">10</span></span>

<span data-ttu-id="02353-142">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="02353-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="02353-143">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="02353-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="02353-144">11</span><span class="sxs-lookup"><span data-stu-id="02353-144">11</span></span>

<span data-ttu-id="02353-145">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="02353-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="02353-146">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="02353-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="02353-147">12</span><span class="sxs-lookup"><span data-stu-id="02353-147">12</span></span>

<span data-ttu-id="02353-148">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="02353-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="02353-149">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="02353-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="02353-150">13</span><span class="sxs-lookup"><span data-stu-id="02353-150">13</span></span>

<span data-ttu-id="02353-151">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="02353-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="02353-152">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="02353-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="02353-153">14</span><span class="sxs-lookup"><span data-stu-id="02353-153">14</span></span>

<span data-ttu-id="02353-154">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="02353-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="02353-155">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="02353-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="02353-156">15</span><span class="sxs-lookup"><span data-stu-id="02353-156">15</span></span>

<span data-ttu-id="02353-157">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="02353-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="02353-158">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="02353-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="02353-159">16</span><span class="sxs-lookup"><span data-stu-id="02353-159">16</span></span>

<span data-ttu-id="02353-160">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02353-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="02353-161">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="02353-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="02353-162">17</span><span class="sxs-lookup"><span data-stu-id="02353-162">17</span></span>

<span data-ttu-id="02353-163">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="02353-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="02353-164">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="02353-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="02353-165">21</span><span class="sxs-lookup"><span data-stu-id="02353-165">21</span></span>

<span data-ttu-id="02353-166">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02353-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02353-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02353-167">Requirements</span></span>



| <span data-ttu-id="02353-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02353-168">Requirement</span></span> | <span data-ttu-id="02353-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="02353-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02353-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02353-170">Minimum supported client</span></span><br/> | <span data-ttu-id="02353-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02353-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02353-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02353-172">Minimum supported server</span></span><br/> | <span data-ttu-id="02353-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02353-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02353-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02353-174">Namespace</span></span><br/>                | <span data-ttu-id="02353-175">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="02353-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02353-176">MOF</span><span class="sxs-lookup"><span data-stu-id="02353-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02353-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02353-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02353-178">DLL</span><span class="sxs-lookup"><span data-stu-id="02353-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02353-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02353-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02353-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02353-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="02353-181">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="02353-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="02353-182">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="02353-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

