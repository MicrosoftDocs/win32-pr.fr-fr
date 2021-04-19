---
description: Modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516386"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="ae66e-103">Méthode ChangeSecurityPermissions de la \_ classe CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="ae66e-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="ae66e-104">La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae66e-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="ae66e-105">Si le fichier logique est un répertoire, **ChangeSecurityPermissions** agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="ae66e-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae66e-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ae66e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ae66e-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ae66e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ae66e-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ae66e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ae66e-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ae66e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae66e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae66e-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="ae66e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae66e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae66e-112">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-113">Spécifie des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ae66e-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="ae66e-114">Une liste de contrôle d’accès (ACL) **null** dans le [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="ae66e-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="ae66e-115">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae66e-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-116">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="ae66e-116">Security privilege to modify.</span></span> <span data-ttu-id="ae66e-117">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ae66e-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="ae66e-118">ou</span><span class="sxs-lookup"><span data-stu-id="ae66e-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="ae66e-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="ae66e-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ae66e-120">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="ae66e-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="ae66e-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="ae66e-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ae66e-122">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="ae66e-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="ae66e-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="ae66e-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ae66e-124">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="ae66e-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="ae66e-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="ae66e-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ae66e-126">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="ae66e-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae66e-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae66e-127">Return value</span></span>

<span data-ttu-id="ae66e-128">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ae66e-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ae66e-129">**Success**</span><span class="sxs-lookup"><span data-stu-id="ae66e-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-130">0</span><span class="sxs-lookup"><span data-stu-id="ae66e-130">0</span></span>

<span data-ttu-id="ae66e-131">Réussite.</span><span class="sxs-lookup"><span data-stu-id="ae66e-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-132">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="ae66e-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-133">2</span><span class="sxs-lookup"><span data-stu-id="ae66e-133">2</span></span>

<span data-ttu-id="ae66e-134">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="ae66e-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-135">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="ae66e-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-136">8</span><span class="sxs-lookup"><span data-stu-id="ae66e-136">8</span></span>

<span data-ttu-id="ae66e-137">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae66e-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-138">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="ae66e-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-139">9</span><span class="sxs-lookup"><span data-stu-id="ae66e-139">9</span></span>

<span data-ttu-id="ae66e-140">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-141">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="ae66e-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-142">10</span><span class="sxs-lookup"><span data-stu-id="ae66e-142">10</span></span>

<span data-ttu-id="ae66e-143">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ae66e-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-144">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="ae66e-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-145">11</span><span class="sxs-lookup"><span data-stu-id="ae66e-145">11</span></span>

<span data-ttu-id="ae66e-146">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="ae66e-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-147">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="ae66e-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-148">12</span><span class="sxs-lookup"><span data-stu-id="ae66e-148">12</span></span>

<span data-ttu-id="ae66e-149">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="ae66e-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-150">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="ae66e-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-151">13</span><span class="sxs-lookup"><span data-stu-id="ae66e-151">13</span></span>

<span data-ttu-id="ae66e-152">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="ae66e-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-153">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="ae66e-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-154">14</span><span class="sxs-lookup"><span data-stu-id="ae66e-154">14</span></span>

<span data-ttu-id="ae66e-155">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-156">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="ae66e-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-157">15</span><span class="sxs-lookup"><span data-stu-id="ae66e-157">15</span></span>

<span data-ttu-id="ae66e-158">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="ae66e-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-159">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="ae66e-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-160">16</span><span class="sxs-lookup"><span data-stu-id="ae66e-160">16</span></span>

<span data-ttu-id="ae66e-161">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-162">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="ae66e-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-163">17</span><span class="sxs-lookup"><span data-stu-id="ae66e-163">17</span></span>

<span data-ttu-id="ae66e-164">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="ae66e-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="ae66e-165">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="ae66e-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ae66e-166">21</span><span class="sxs-lookup"><span data-stu-id="ae66e-166">21</span></span>

<span data-ttu-id="ae66e-167">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="ae66e-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae66e-168">Notes</span><span class="sxs-lookup"><span data-stu-id="ae66e-168">Remarks</span></span>

<span data-ttu-id="ae66e-169">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="ae66e-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ae66e-170">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ae66e-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ae66e-171">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ae66e-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ae66e-172">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ae66e-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae66e-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae66e-173">Requirements</span></span>



| <span data-ttu-id="ae66e-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae66e-174">Requirement</span></span> | <span data-ttu-id="ae66e-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae66e-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae66e-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae66e-176">Minimum supported client</span></span><br/> | <span data-ttu-id="ae66e-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae66e-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae66e-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae66e-178">Minimum supported server</span></span><br/> | <span data-ttu-id="ae66e-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae66e-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae66e-180">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ae66e-180">Namespace</span></span><br/>                | <span data-ttu-id="ae66e-181">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ae66e-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae66e-182">MOF</span><span class="sxs-lookup"><span data-stu-id="ae66e-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae66e-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae66e-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae66e-184">DLL</span><span class="sxs-lookup"><span data-stu-id="ae66e-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae66e-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae66e-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae66e-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae66e-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae66e-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae66e-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="ae66e-188">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae66e-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

