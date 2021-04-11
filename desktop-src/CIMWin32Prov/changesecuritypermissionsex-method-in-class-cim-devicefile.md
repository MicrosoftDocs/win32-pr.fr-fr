---
description: Modifie les autorisations de sécurité pour le fichier d’appareil spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110974"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="6660c-103">Méthode ChangeSecurityPermissionsEx de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="6660c-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="6660c-104">La méthode **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier d’appareil spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) ).</span><span class="sxs-lookup"><span data-stu-id="6660c-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="6660c-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="6660c-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="6660c-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6660c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6660c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6660c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6660c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6660c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6660c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6660c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6660c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6660c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6660c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6660c-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6660c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6660c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6660c-113">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6660c-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6660c-114">Spécifie les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6660c-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="6660c-115">Une ACL **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="6660c-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="6660c-116">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6660c-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6660c-117">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="6660c-117">Security privilege to modify.</span></span> <span data-ttu-id="6660c-118">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez</span><span class="sxs-lookup"><span data-stu-id="6660c-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="6660c-119">ou</span><span class="sxs-lookup"><span data-stu-id="6660c-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6660c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="6660c-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6660c-121">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6660c-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6660c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="6660c-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6660c-123">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6660c-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6660c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="6660c-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6660c-125">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6660c-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6660c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="6660c-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6660c-127">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="6660c-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6660c-128">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6660c-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6660c-129">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="6660c-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="6660c-130">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="6660c-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6660c-131">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6660c-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6660c-132">Fichier enfant (ou répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6660c-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="6660c-133">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="6660c-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6660c-134">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="6660c-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="6660c-135">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6660c-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6660c-136">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="6660c-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="6660c-137">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6660c-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6660c-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6660c-138">Return value</span></span>

<span data-ttu-id="6660c-139">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="6660c-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="6660c-140">0</span><span class="sxs-lookup"><span data-stu-id="6660c-140">0</span></span>

<span data-ttu-id="6660c-141">Réussite.</span><span class="sxs-lookup"><span data-stu-id="6660c-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-142">2</span><span class="sxs-lookup"><span data-stu-id="6660c-142">2</span></span>

<span data-ttu-id="6660c-143">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="6660c-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-144">8</span><span class="sxs-lookup"><span data-stu-id="6660c-144">8</span></span>

<span data-ttu-id="6660c-145">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="6660c-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-146">9</span><span class="sxs-lookup"><span data-stu-id="6660c-146">9</span></span>

<span data-ttu-id="6660c-147">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="6660c-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-148">10</span><span class="sxs-lookup"><span data-stu-id="6660c-148">10</span></span>

<span data-ttu-id="6660c-149">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6660c-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-150">11</span><span class="sxs-lookup"><span data-stu-id="6660c-150">11</span></span>

<span data-ttu-id="6660c-151">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="6660c-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-152">12</span><span class="sxs-lookup"><span data-stu-id="6660c-152">12</span></span>

<span data-ttu-id="6660c-153">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="6660c-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-154">13</span><span class="sxs-lookup"><span data-stu-id="6660c-154">13</span></span>

<span data-ttu-id="6660c-155">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="6660c-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-156">14</span><span class="sxs-lookup"><span data-stu-id="6660c-156">14</span></span>

<span data-ttu-id="6660c-157">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6660c-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-158">15</span><span class="sxs-lookup"><span data-stu-id="6660c-158">15</span></span>

<span data-ttu-id="6660c-159">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="6660c-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-160">16</span><span class="sxs-lookup"><span data-stu-id="6660c-160">16</span></span>

<span data-ttu-id="6660c-161">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="6660c-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-162">17</span><span class="sxs-lookup"><span data-stu-id="6660c-162">17</span></span>

<span data-ttu-id="6660c-163">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="6660c-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="6660c-164">21</span><span class="sxs-lookup"><span data-stu-id="6660c-164">21</span></span>

<span data-ttu-id="6660c-165">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="6660c-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6660c-166">Notes</span><span class="sxs-lookup"><span data-stu-id="6660c-166">Remarks</span></span>

<span data-ttu-id="6660c-167">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="6660c-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6660c-168">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6660c-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6660c-169">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6660c-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6660c-170">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6660c-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6660c-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6660c-171">Requirements</span></span>



| <span data-ttu-id="6660c-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6660c-172">Requirement</span></span> | <span data-ttu-id="6660c-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="6660c-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6660c-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6660c-174">Minimum supported client</span></span><br/> | <span data-ttu-id="6660c-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6660c-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6660c-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6660c-176">Minimum supported server</span></span><br/> | <span data-ttu-id="6660c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6660c-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6660c-178">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6660c-178">Namespace</span></span><br/>                | <span data-ttu-id="6660c-179">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6660c-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6660c-180">MOF</span><span class="sxs-lookup"><span data-stu-id="6660c-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6660c-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6660c-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6660c-182">DLL</span><span class="sxs-lookup"><span data-stu-id="6660c-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6660c-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6660c-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6660c-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6660c-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6660c-185">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="6660c-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="6660c-186">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="6660c-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

