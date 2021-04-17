---
description: Modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode ChangeSecurityPermissions).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissionsEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523796"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="8d997-103">Méthode ChangeSecurityPermissionsEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="8d997-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="8d997-104">La méthode **ChangeSecurityPermissionsEX** modifie les autorisations de sécurité pour le fichier de données logiques spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) ).</span><span class="sxs-lookup"><span data-stu-id="8d997-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="8d997-105">Si le fichier logique est effectivement un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="8d997-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d997-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="8d997-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d997-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d997-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d997-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8d997-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8d997-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8d997-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d997-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d997-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8d997-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d997-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d997-112">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d997-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d997-113">Spécifie des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8d997-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="8d997-114">Une ACL **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="8d997-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="8d997-115">Pour plus d’informations sur les implications d’un accès illimité, consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="8d997-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="8d997-116">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d997-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d997-117">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="8d997-117">Security privilege to modify.</span></span> <span data-ttu-id="8d997-118">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="8d997-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="8d997-119">`Option = 1 + 4` ou `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="8d997-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="8d997-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="8d997-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8d997-121">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d997-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="8d997-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="8d997-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8d997-123">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d997-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="8d997-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="8d997-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8d997-125">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d997-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="8d997-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="8d997-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8d997-127">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="8d997-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8d997-128">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d997-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d997-129">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="8d997-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8d997-130">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="8d997-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-131">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8d997-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d997-132">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8d997-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8d997-133">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="8d997-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8d997-134">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="8d997-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="8d997-135">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="8d997-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-136">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8d997-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d997-137">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du fichier de [**\_ fichier CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="8d997-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="8d997-138">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8d997-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d997-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d997-139">Return value</span></span>

<span data-ttu-id="8d997-140">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8d997-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="8d997-141">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8d997-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8d997-142">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8d997-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8d997-143">**Success**</span><span class="sxs-lookup"><span data-stu-id="8d997-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-144">0</span><span class="sxs-lookup"><span data-stu-id="8d997-144">0</span></span>

<span data-ttu-id="8d997-145">Réussite.</span><span class="sxs-lookup"><span data-stu-id="8d997-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-146">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="8d997-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-147">2</span><span class="sxs-lookup"><span data-stu-id="8d997-147">2</span></span>

<span data-ttu-id="8d997-148">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8d997-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-149">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="8d997-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-150">8</span><span class="sxs-lookup"><span data-stu-id="8d997-150">8</span></span>

<span data-ttu-id="8d997-151">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d997-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-152">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="8d997-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-153">9</span><span class="sxs-lookup"><span data-stu-id="8d997-153">9</span></span>

<span data-ttu-id="8d997-154">Le nom d’objet spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8d997-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-155">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="8d997-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-156">10</span><span class="sxs-lookup"><span data-stu-id="8d997-156">10</span></span>

<span data-ttu-id="8d997-157">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8d997-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-158">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="8d997-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-159">11</span><span class="sxs-lookup"><span data-stu-id="8d997-159">11</span></span>

<span data-ttu-id="8d997-160">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="8d997-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-161">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="8d997-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-162">12</span><span class="sxs-lookup"><span data-stu-id="8d997-162">12</span></span>

<span data-ttu-id="8d997-163">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="8d997-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-164">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="8d997-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-165">13</span><span class="sxs-lookup"><span data-stu-id="8d997-165">13</span></span>

<span data-ttu-id="8d997-166">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="8d997-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-167">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="8d997-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-168">14</span><span class="sxs-lookup"><span data-stu-id="8d997-168">14</span></span>

<span data-ttu-id="8d997-169">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="8d997-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-170">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="8d997-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-171">15</span><span class="sxs-lookup"><span data-stu-id="8d997-171">15</span></span>

<span data-ttu-id="8d997-172">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="8d997-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-173">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="8d997-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-174">16</span><span class="sxs-lookup"><span data-stu-id="8d997-174">16</span></span>

<span data-ttu-id="8d997-175">Le fichier de démarrage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8d997-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-176">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="8d997-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-177">17</span><span class="sxs-lookup"><span data-stu-id="8d997-177">17</span></span>

<span data-ttu-id="8d997-178">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="8d997-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8d997-179">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="8d997-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8d997-180">21</span><span class="sxs-lookup"><span data-stu-id="8d997-180">21</span></span>

<span data-ttu-id="8d997-181">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8d997-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d997-182">Notes</span><span class="sxs-lookup"><span data-stu-id="8d997-182">Remarks</span></span>

<span data-ttu-id="8d997-183">La méthode **ChangeSecurityPermissionsEX** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="8d997-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="8d997-184">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d997-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d997-185">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8d997-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d997-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d997-186">Requirements</span></span>



| <span data-ttu-id="8d997-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d997-187">Requirement</span></span> | <span data-ttu-id="8d997-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d997-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d997-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d997-189">Minimum supported client</span></span><br/> | <span data-ttu-id="8d997-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d997-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d997-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d997-191">Minimum supported server</span></span><br/> | <span data-ttu-id="8d997-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d997-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d997-193">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d997-193">Namespace</span></span><br/>                | <span data-ttu-id="8d997-194">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8d997-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d997-195">MOF</span><span class="sxs-lookup"><span data-stu-id="8d997-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d997-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d997-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d997-197">DLL</span><span class="sxs-lookup"><span data-stu-id="8d997-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d997-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d997-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d997-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d997-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d997-200">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="8d997-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8d997-201">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="8d997-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8d997-202">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="8d997-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="8d997-203">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="8d997-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

