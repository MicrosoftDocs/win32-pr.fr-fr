---
description: Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523511"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="11629-103">Méthode ChangeSecurityPermissionsEx de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="11629-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="11629-104">La méthode **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ).</span><span class="sxs-lookup"><span data-stu-id="11629-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="11629-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="11629-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11629-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="11629-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="11629-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="11629-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="11629-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="11629-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11629-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="11629-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11629-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11629-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="11629-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11629-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11629-112">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11629-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11629-113">Spécifie les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="11629-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="11629-114">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11629-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11629-115">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="11629-115">Security privilege to modify.</span></span> <span data-ttu-id="11629-116">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez</span><span class="sxs-lookup"><span data-stu-id="11629-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="11629-117">ou</span><span class="sxs-lookup"><span data-stu-id="11629-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="11629-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="11629-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="11629-119">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="11629-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="11629-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="11629-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="11629-121">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="11629-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="11629-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="11629-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="11629-123">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="11629-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="11629-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="11629-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="11629-125">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="11629-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="11629-126">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11629-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11629-127">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="11629-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="11629-128">Ce paramètre a une valeur **null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="11629-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="11629-129">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="11629-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11629-130">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="11629-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="11629-131">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="11629-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="11629-132">Si la valeur du paramètre est **null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="11629-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="11629-133">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="11629-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="11629-134">Si la **valeur est true**, les autorisations de sécurité sont appliquées de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="11629-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="11629-135">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="11629-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11629-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11629-136">Return value</span></span>

<span data-ttu-id="11629-137">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="11629-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="11629-138">**Success**</span><span class="sxs-lookup"><span data-stu-id="11629-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="11629-139">0</span><span class="sxs-lookup"><span data-stu-id="11629-139">0</span></span>

<span data-ttu-id="11629-140">Réussite.</span><span class="sxs-lookup"><span data-stu-id="11629-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="11629-141">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="11629-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="11629-142">2</span><span class="sxs-lookup"><span data-stu-id="11629-142">2</span></span>

<span data-ttu-id="11629-143">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="11629-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="11629-144">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="11629-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="11629-145">8</span><span class="sxs-lookup"><span data-stu-id="11629-145">8</span></span>

<span data-ttu-id="11629-146">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="11629-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="11629-147">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="11629-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="11629-148">9</span><span class="sxs-lookup"><span data-stu-id="11629-148">9</span></span>

<span data-ttu-id="11629-149">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="11629-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="11629-150">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="11629-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="11629-151">10</span><span class="sxs-lookup"><span data-stu-id="11629-151">10</span></span>

<span data-ttu-id="11629-152">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="11629-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="11629-153">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="11629-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="11629-154">11</span><span class="sxs-lookup"><span data-stu-id="11629-154">11</span></span>

<span data-ttu-id="11629-155">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="11629-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="11629-156">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="11629-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="11629-157">12</span><span class="sxs-lookup"><span data-stu-id="11629-157">12</span></span>

<span data-ttu-id="11629-158">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="11629-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="11629-159">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="11629-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="11629-160">13</span><span class="sxs-lookup"><span data-stu-id="11629-160">13</span></span>

<span data-ttu-id="11629-161">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="11629-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="11629-162">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="11629-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="11629-163">14</span><span class="sxs-lookup"><span data-stu-id="11629-163">14</span></span>

<span data-ttu-id="11629-164">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="11629-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="11629-165">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="11629-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="11629-166">15</span><span class="sxs-lookup"><span data-stu-id="11629-166">15</span></span>

<span data-ttu-id="11629-167">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="11629-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="11629-168">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="11629-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="11629-169">16</span><span class="sxs-lookup"><span data-stu-id="11629-169">16</span></span>

<span data-ttu-id="11629-170">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="11629-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="11629-171">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="11629-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="11629-172">17</span><span class="sxs-lookup"><span data-stu-id="11629-172">17</span></span>

<span data-ttu-id="11629-173">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="11629-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="11629-174">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="11629-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="11629-175">21</span><span class="sxs-lookup"><span data-stu-id="11629-175">21</span></span>

<span data-ttu-id="11629-176">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="11629-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11629-177">Notes</span><span class="sxs-lookup"><span data-stu-id="11629-177">Remarks</span></span>

<span data-ttu-id="11629-178">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="11629-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="11629-179">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="11629-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="11629-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11629-180">Requirements</span></span>



| <span data-ttu-id="11629-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11629-181">Requirement</span></span> | <span data-ttu-id="11629-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="11629-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11629-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11629-183">Minimum supported client</span></span><br/> | <span data-ttu-id="11629-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11629-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11629-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11629-185">Minimum supported server</span></span><br/> | <span data-ttu-id="11629-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11629-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11629-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11629-187">Namespace</span></span><br/>                | <span data-ttu-id="11629-188">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="11629-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11629-189">MOF</span><span class="sxs-lookup"><span data-stu-id="11629-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11629-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11629-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11629-191">DLL</span><span class="sxs-lookup"><span data-stu-id="11629-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11629-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11629-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11629-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11629-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11629-194">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="11629-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="11629-195">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="11629-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

