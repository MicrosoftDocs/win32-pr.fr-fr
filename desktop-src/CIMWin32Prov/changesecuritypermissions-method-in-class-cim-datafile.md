---
description: Modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111006"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="23bbc-103">Méthode ChangeSecurityPermissions de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="23bbc-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="23bbc-104">La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="23bbc-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="23bbc-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="23bbc-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="23bbc-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="23bbc-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23bbc-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="23bbc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23bbc-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23bbc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23bbc-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="23bbc-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="23bbc-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="23bbc-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="23bbc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23bbc-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="23bbc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23bbc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23bbc-113">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23bbc-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-114">Spécifie les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="23bbc-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="23bbc-115">Une liste de contrôle d’accès (ACL) **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="23bbc-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="23bbc-116">Pour plus d’informations sur les implications d’un accès illimité, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="23bbc-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="23bbc-117">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23bbc-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-118">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="23bbc-118">Security privilege to modify.</span></span> <span data-ttu-id="23bbc-119">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="23bbc-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="23bbc-120">ou</span><span class="sxs-lookup"><span data-stu-id="23bbc-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="23bbc-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="23bbc-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23bbc-122">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="23bbc-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="23bbc-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="23bbc-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23bbc-124">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="23bbc-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="23bbc-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="23bbc-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23bbc-126">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="23bbc-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="23bbc-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="23bbc-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="23bbc-128">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="23bbc-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23bbc-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23bbc-129">Return value</span></span>

<span data-ttu-id="23bbc-130">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="23bbc-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="23bbc-131">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="23bbc-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="23bbc-132">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="23bbc-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="23bbc-133">**Success**</span><span class="sxs-lookup"><span data-stu-id="23bbc-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-134">0</span><span class="sxs-lookup"><span data-stu-id="23bbc-134">0</span></span>

<span data-ttu-id="23bbc-135">Réussite.</span><span class="sxs-lookup"><span data-stu-id="23bbc-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-136">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="23bbc-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-137">2</span><span class="sxs-lookup"><span data-stu-id="23bbc-137">2</span></span>

<span data-ttu-id="23bbc-138">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="23bbc-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-139">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="23bbc-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-140">8</span><span class="sxs-lookup"><span data-stu-id="23bbc-140">8</span></span>

<span data-ttu-id="23bbc-141">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="23bbc-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-142">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="23bbc-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-143">9</span><span class="sxs-lookup"><span data-stu-id="23bbc-143">9</span></span>

<span data-ttu-id="23bbc-144">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="23bbc-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-145">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="23bbc-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-146">10</span><span class="sxs-lookup"><span data-stu-id="23bbc-146">10</span></span>

<span data-ttu-id="23bbc-147">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="23bbc-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-148">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="23bbc-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-149">11</span><span class="sxs-lookup"><span data-stu-id="23bbc-149">11</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-150">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="23bbc-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-151">12</span><span class="sxs-lookup"><span data-stu-id="23bbc-151">12</span></span>

<span data-ttu-id="23bbc-152">Plateforme non basée sur Windows NT.</span><span class="sxs-lookup"><span data-stu-id="23bbc-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-153">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="23bbc-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-154">13</span><span class="sxs-lookup"><span data-stu-id="23bbc-154">13</span></span>

<span data-ttu-id="23bbc-155">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="23bbc-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-156">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="23bbc-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-157">14</span><span class="sxs-lookup"><span data-stu-id="23bbc-157">14</span></span>

<span data-ttu-id="23bbc-158">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="23bbc-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-159">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="23bbc-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-160">15</span><span class="sxs-lookup"><span data-stu-id="23bbc-160">15</span></span>

<span data-ttu-id="23bbc-161">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="23bbc-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-162">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="23bbc-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-163">16</span><span class="sxs-lookup"><span data-stu-id="23bbc-163">16</span></span>

<span data-ttu-id="23bbc-164">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="23bbc-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-165">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="23bbc-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-166">17</span><span class="sxs-lookup"><span data-stu-id="23bbc-166">17</span></span>

<span data-ttu-id="23bbc-167">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="23bbc-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="23bbc-168">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="23bbc-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="23bbc-169">21</span><span class="sxs-lookup"><span data-stu-id="23bbc-169">21</span></span>

<span data-ttu-id="23bbc-170">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="23bbc-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23bbc-171">Notes</span><span class="sxs-lookup"><span data-stu-id="23bbc-171">Remarks</span></span>

<span data-ttu-id="23bbc-172">La méthode **ChangeSecurityPermissions** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="23bbc-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="23bbc-173">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="23bbc-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23bbc-174">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="23bbc-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23bbc-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23bbc-175">Requirements</span></span>



| <span data-ttu-id="23bbc-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23bbc-176">Requirement</span></span> | <span data-ttu-id="23bbc-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="23bbc-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23bbc-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23bbc-178">Minimum supported client</span></span><br/> | <span data-ttu-id="23bbc-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23bbc-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23bbc-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23bbc-180">Minimum supported server</span></span><br/> | <span data-ttu-id="23bbc-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23bbc-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23bbc-182">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23bbc-182">Namespace</span></span><br/>                | <span data-ttu-id="23bbc-183">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="23bbc-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23bbc-184">MOF</span><span class="sxs-lookup"><span data-stu-id="23bbc-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23bbc-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23bbc-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23bbc-186">DLL</span><span class="sxs-lookup"><span data-stu-id="23bbc-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23bbc-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23bbc-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23bbc-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23bbc-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bbc-189">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="23bbc-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="23bbc-190">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="23bbc-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="23bbc-191">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="23bbc-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="23bbc-192">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="23bbc-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

