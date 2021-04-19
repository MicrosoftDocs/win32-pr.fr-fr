---
description: Modifie les autorisations de sécurité pour le fichier de codec logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517390"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a><span data-ttu-id="0b5f4-103">Méthode ChangeSecurityPermissions de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="0b5f4-103">ChangeSecurityPermissions method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="0b5f4-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de codec logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical codec file specified in the object path.</span></span> <span data-ttu-id="0b5f4-105">Si le fichier logique est un répertoire, **ChangeSecurityPermissions** est récursif et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories the directory contains.</span></span> <span data-ttu-id="0b5f4-106">**ChangeSecurityPermissions** retourne une valeur entière égale à 0 (zéro) si les autorisations sont modifiées, et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="0b5f4-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0b5f4-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b5f4-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b5f4-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b5f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b5f4-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="0b5f4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b5f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b5f4-111">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b5f4-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-112">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="0b5f4-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="0b5f4-113">Ce descripteur contient de nouvelles autorisations de sécurité pour l’instance de [**Win32 \_ CodecFile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="0b5f4-113">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-114">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b5f4-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-115">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-115">Security privilege to be modified.</span></span> <span data-ttu-id="0b5f4-116">Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez :</span><span class="sxs-lookup"><span data-stu-id="0b5f4-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="0b5f4-117">-ou-</span><span class="sxs-lookup"><span data-stu-id="0b5f4-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="0b5f4-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="0b5f4-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="0b5f4-119">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="0b5f4-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ GROUPEr les \_ \_ informations de sécurité** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="0b5f4-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="0b5f4-121">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="0b5f4-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="0b5f4-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="0b5f4-123">Modifiez la liste de contrôle d’accès discrétionnaire (DACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="0b5f4-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="0b5f4-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="0b5f4-125">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b5f4-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b5f4-126">Return value</span></span>

<span data-ttu-id="0b5f4-127">Retourne une valeur 0 (zéro) si les autorisations sont modifiées et un nombre différent pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-127">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0b5f4-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-129">0</span><span class="sxs-lookup"><span data-stu-id="0b5f4-129">0</span></span>

<span data-ttu-id="0b5f4-130">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-131">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-132">2</span><span class="sxs-lookup"><span data-stu-id="0b5f4-132">2</span></span>

<span data-ttu-id="0b5f4-133">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-134">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-135">8</span><span class="sxs-lookup"><span data-stu-id="0b5f4-135">8</span></span>

<span data-ttu-id="0b5f4-136">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-137">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-138">9</span><span class="sxs-lookup"><span data-stu-id="0b5f4-138">9</span></span>

<span data-ttu-id="0b5f4-139">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-140">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-141">10</span><span class="sxs-lookup"><span data-stu-id="0b5f4-141">10</span></span>

<span data-ttu-id="0b5f4-142">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-143">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-144">11</span><span class="sxs-lookup"><span data-stu-id="0b5f4-144">11</span></span>

<span data-ttu-id="0b5f4-145">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-146">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-147">12</span><span class="sxs-lookup"><span data-stu-id="0b5f4-147">12</span></span>

<span data-ttu-id="0b5f4-148">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-149">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-150">13</span><span class="sxs-lookup"><span data-stu-id="0b5f4-150">13</span></span>

<span data-ttu-id="0b5f4-151">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-152">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-153">14</span><span class="sxs-lookup"><span data-stu-id="0b5f4-153">14</span></span>

<span data-ttu-id="0b5f4-154">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-155">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-156">15</span><span class="sxs-lookup"><span data-stu-id="0b5f4-156">15</span></span>

<span data-ttu-id="0b5f4-157">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-158">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-159">16</span><span class="sxs-lookup"><span data-stu-id="0b5f4-159">16</span></span>

<span data-ttu-id="0b5f4-160">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-161">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-162">17</span><span class="sxs-lookup"><span data-stu-id="0b5f4-162">17</span></span>

<span data-ttu-id="0b5f4-163">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0b5f4-164">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0b5f4-165">21</span><span class="sxs-lookup"><span data-stu-id="0b5f4-165">21</span></span>

<span data-ttu-id="0b5f4-166">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b5f4-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b5f4-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b5f4-167">Requirements</span></span>



| <span data-ttu-id="0b5f4-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b5f4-168">Requirement</span></span> | <span data-ttu-id="0b5f4-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b5f4-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5f4-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b5f4-170">Minimum supported client</span></span><br/> | <span data-ttu-id="0b5f4-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b5f4-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b5f4-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b5f4-172">Minimum supported server</span></span><br/> | <span data-ttu-id="0b5f4-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b5f4-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b5f4-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b5f4-174">Namespace</span></span><br/>                | <span data-ttu-id="0b5f4-175">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0b5f4-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b5f4-176">MOF</span><span class="sxs-lookup"><span data-stu-id="0b5f4-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b5f4-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b5f4-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b5f4-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0b5f4-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b5f4-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b5f4-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b5f4-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b5f4-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b5f4-181">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b5f4-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b5f4-182">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="0b5f4-182">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

