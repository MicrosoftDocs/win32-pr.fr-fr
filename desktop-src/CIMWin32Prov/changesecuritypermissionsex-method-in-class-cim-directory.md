---
description: Modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions et est héritée de CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515930"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="957c4-103">Méthode ChangeSecurityPermissionsEx de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="957c4-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="957c4-104">La méthode **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) et est héritée de [**CIM \_ LogicalFile**](cim-logicalfile.md)).</span><span class="sxs-lookup"><span data-stu-id="957c4-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="957c4-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="957c4-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="957c4-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="957c4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="957c4-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="957c4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="957c4-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="957c4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="957c4-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="957c4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="957c4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="957c4-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="957c4-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="957c4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957c4-112">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="957c4-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="957c4-113">Spécifie des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="957c4-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="957c4-114">Une ACL **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="957c4-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="957c4-115">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="957c4-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="957c4-116">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="957c4-116">Security privilege to modify.</span></span> <span data-ttu-id="957c4-117">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez</span><span class="sxs-lookup"><span data-stu-id="957c4-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="957c4-118">ou</span><span class="sxs-lookup"><span data-stu-id="957c4-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="957c4-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="957c4-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="957c4-120">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="957c4-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="957c4-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="957c4-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="957c4-122">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="957c4-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="957c4-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="957c4-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="957c4-124">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="957c4-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="957c4-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="957c4-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="957c4-126">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="957c4-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="957c4-127">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="957c4-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="957c4-128">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="957c4-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="957c4-129">Ce paramètre a une valeur **null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="957c4-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="957c4-130">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="957c4-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="957c4-131">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="957c4-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="957c4-132">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="957c4-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="957c4-133">Si la valeur du paramètre est **null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="957c4-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="957c4-134">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="957c4-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="957c4-135">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance de [**\_ répertoire CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="957c4-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="957c4-136">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="957c4-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957c4-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="957c4-137">Return value</span></span>

<span data-ttu-id="957c4-138">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="957c4-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="957c4-139">0</span><span class="sxs-lookup"><span data-stu-id="957c4-139">0</span></span>

<span data-ttu-id="957c4-140">Réussite.</span><span class="sxs-lookup"><span data-stu-id="957c4-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-141">2</span><span class="sxs-lookup"><span data-stu-id="957c4-141">2</span></span>

<span data-ttu-id="957c4-142">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="957c4-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-143">8</span><span class="sxs-lookup"><span data-stu-id="957c4-143">8</span></span>

<span data-ttu-id="957c4-144">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="957c4-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-145">9</span><span class="sxs-lookup"><span data-stu-id="957c4-145">9</span></span>

<span data-ttu-id="957c4-146">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="957c4-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-147">10</span><span class="sxs-lookup"><span data-stu-id="957c4-147">10</span></span>

<span data-ttu-id="957c4-148">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="957c4-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-149">11</span><span class="sxs-lookup"><span data-stu-id="957c4-149">11</span></span>

<span data-ttu-id="957c4-150">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="957c4-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-151">12</span><span class="sxs-lookup"><span data-stu-id="957c4-151">12</span></span>

<span data-ttu-id="957c4-152">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="957c4-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-153">13</span><span class="sxs-lookup"><span data-stu-id="957c4-153">13</span></span>

<span data-ttu-id="957c4-154">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="957c4-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-155">14</span><span class="sxs-lookup"><span data-stu-id="957c4-155">14</span></span>

<span data-ttu-id="957c4-156">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="957c4-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-157">15</span><span class="sxs-lookup"><span data-stu-id="957c4-157">15</span></span>

<span data-ttu-id="957c4-158">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="957c4-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-159">16</span><span class="sxs-lookup"><span data-stu-id="957c4-159">16</span></span>

<span data-ttu-id="957c4-160">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="957c4-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-161">17</span><span class="sxs-lookup"><span data-stu-id="957c4-161">17</span></span>

<span data-ttu-id="957c4-162">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="957c4-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="957c4-163">21</span><span class="sxs-lookup"><span data-stu-id="957c4-163">21</span></span>

<span data-ttu-id="957c4-164">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="957c4-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="957c4-165">Notes</span><span class="sxs-lookup"><span data-stu-id="957c4-165">Remarks</span></span>

<span data-ttu-id="957c4-166">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="957c4-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="957c4-167">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="957c4-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="957c4-168">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="957c4-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="957c4-169">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="957c4-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="957c4-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="957c4-170">Requirements</span></span>



| <span data-ttu-id="957c4-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="957c4-171">Requirement</span></span> | <span data-ttu-id="957c4-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="957c4-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="957c4-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="957c4-173">Minimum supported client</span></span><br/> | <span data-ttu-id="957c4-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="957c4-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="957c4-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="957c4-175">Minimum supported server</span></span><br/> | <span data-ttu-id="957c4-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="957c4-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="957c4-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="957c4-177">Namespace</span></span><br/>                | <span data-ttu-id="957c4-178">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="957c4-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="957c4-179">MOF</span><span class="sxs-lookup"><span data-stu-id="957c4-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="957c4-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="957c4-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="957c4-181">DLL</span><span class="sxs-lookup"><span data-stu-id="957c4-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="957c4-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="957c4-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957c4-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="957c4-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957c4-184">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="957c4-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="957c4-185">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="957c4-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

