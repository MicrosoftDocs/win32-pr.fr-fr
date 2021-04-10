---
description: Modifie les autorisations de sécurité pour le fichier d’échange logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950688"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="50d31-103">Méthode ChangeSecurityPermissions de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="50d31-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="50d31-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de pagination logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="50d31-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="50d31-105">Si le fichier logique est un répertoire, **ChangeSecurityPermissions** est récursif et modifie les autorisations de sécurité de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="50d31-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="50d31-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="50d31-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="50d31-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="50d31-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="50d31-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50d31-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="50d31-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50d31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d31-110">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50d31-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d31-111">Expression qui correspond à une instance de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="50d31-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="50d31-112">Ce descripteur contient de nouvelles autorisations de sécurité pour l’instance du [**\_ fichier d’échange Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="50d31-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="50d31-113">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50d31-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d31-114">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="50d31-114">Security privilege to be modified.</span></span> <span data-ttu-id="50d31-115">Par exemple, pour modifier la sécurité du propriétaire et de la liste de contrôle d’accès discrétionnaire (DACL), utilisez :</span><span class="sxs-lookup"><span data-stu-id="50d31-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="50d31-116">-ou-</span><span class="sxs-lookup"><span data-stu-id="50d31-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="50d31-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="50d31-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="50d31-118">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="50d31-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="50d31-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="50d31-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="50d31-120">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="50d31-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="50d31-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="50d31-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="50d31-122">Modifiez la liste DACL du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="50d31-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="50d31-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="50d31-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="50d31-124">Modifiez la liste de contrôle d’accès système (SACL) du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="50d31-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d31-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50d31-125">Return value</span></span>

<span data-ttu-id="50d31-126">Retourne la valeur 0 (zéro) si les autorisations sont modifiées et un autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="50d31-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="50d31-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="50d31-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-128">0</span><span class="sxs-lookup"><span data-stu-id="50d31-128">0</span></span>

<span data-ttu-id="50d31-129">La demande a réussi.</span><span class="sxs-lookup"><span data-stu-id="50d31-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-130">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="50d31-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-131">2</span><span class="sxs-lookup"><span data-stu-id="50d31-131">2</span></span>

<span data-ttu-id="50d31-132">L’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="50d31-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-133">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="50d31-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-134">8</span><span class="sxs-lookup"><span data-stu-id="50d31-134">8</span></span>

<span data-ttu-id="50d31-135">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="50d31-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-136">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="50d31-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-137">9</span><span class="sxs-lookup"><span data-stu-id="50d31-137">9</span></span>

<span data-ttu-id="50d31-138">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="50d31-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-139">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="50d31-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-140">10</span><span class="sxs-lookup"><span data-stu-id="50d31-140">10</span></span>

<span data-ttu-id="50d31-141">L'objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="50d31-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-142">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="50d31-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-143">11</span><span class="sxs-lookup"><span data-stu-id="50d31-143">11</span></span>

<span data-ttu-id="50d31-144">Le système de fichiers n’est pas un système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="50d31-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-145">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="50d31-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-146">12</span><span class="sxs-lookup"><span data-stu-id="50d31-146">12</span></span>

<span data-ttu-id="50d31-147">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="50d31-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-148">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="50d31-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-149">13</span><span class="sxs-lookup"><span data-stu-id="50d31-149">13</span></span>

<span data-ttu-id="50d31-150">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="50d31-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-151">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="50d31-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-152">14</span><span class="sxs-lookup"><span data-stu-id="50d31-152">14</span></span>

<span data-ttu-id="50d31-153">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="50d31-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-154">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="50d31-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-155">15</span><span class="sxs-lookup"><span data-stu-id="50d31-155">15</span></span>

<span data-ttu-id="50d31-156">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="50d31-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-157">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="50d31-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-158">16</span><span class="sxs-lookup"><span data-stu-id="50d31-158">16</span></span>

<span data-ttu-id="50d31-159">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="50d31-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-160">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="50d31-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-161">17</span><span class="sxs-lookup"><span data-stu-id="50d31-161">17</span></span>

<span data-ttu-id="50d31-162">Un privilège requis pour l’opération est manquant.</span><span class="sxs-lookup"><span data-stu-id="50d31-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="50d31-163">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="50d31-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="50d31-164">21</span><span class="sxs-lookup"><span data-stu-id="50d31-164">21</span></span>

<span data-ttu-id="50d31-165">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="50d31-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50d31-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d31-166">Requirements</span></span>



| <span data-ttu-id="50d31-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d31-167">Requirement</span></span> | <span data-ttu-id="50d31-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d31-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d31-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d31-169">Minimum supported client</span></span><br/> | <span data-ttu-id="50d31-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50d31-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50d31-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d31-171">Minimum supported server</span></span><br/> | <span data-ttu-id="50d31-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50d31-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50d31-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="50d31-173">Namespace</span></span><br/>                | <span data-ttu-id="50d31-174">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="50d31-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50d31-175">MOF</span><span class="sxs-lookup"><span data-stu-id="50d31-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50d31-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50d31-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50d31-177">DLL</span><span class="sxs-lookup"><span data-stu-id="50d31-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d31-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d31-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d31-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d31-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="50d31-180">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50d31-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="50d31-181">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="50d31-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

