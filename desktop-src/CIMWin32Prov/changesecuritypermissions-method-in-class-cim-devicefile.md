---
description: Modifie les autorisations de sécurité pour le fichier d’unité logique spécifié dans le chemin d’accès de l’objet.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483560"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="83487-103">Méthode ChangeSecurityPermissions de la \_ classe CIM DeviceFile</span><span class="sxs-lookup"><span data-stu-id="83487-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="83487-104">La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier d’unité logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="83487-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="83487-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="83487-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="83487-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="83487-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83487-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="83487-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="83487-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="83487-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="83487-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="83487-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="83487-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="83487-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="83487-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83487-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="83487-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83487-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83487-113">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83487-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83487-114">Spécifie les informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="83487-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="83487-115">Une liste de contrôle d’accès (ACL) **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="83487-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="83487-116">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83487-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83487-117">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="83487-117">Security privilege to modify.</span></span> <span data-ttu-id="83487-118">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="83487-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="83487-119">ou</span><span class="sxs-lookup"><span data-stu-id="83487-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="83487-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="83487-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="83487-121">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="83487-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="83487-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="83487-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="83487-123">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="83487-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="83487-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="83487-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="83487-125">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="83487-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="83487-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="83487-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="83487-127">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="83487-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83487-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83487-128">Return value</span></span>

<span data-ttu-id="83487-129">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="83487-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="83487-130">**Success**</span><span class="sxs-lookup"><span data-stu-id="83487-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="83487-131">0</span><span class="sxs-lookup"><span data-stu-id="83487-131">0</span></span>

<span data-ttu-id="83487-132">Réussite.</span><span class="sxs-lookup"><span data-stu-id="83487-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="83487-133">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="83487-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="83487-134">2</span><span class="sxs-lookup"><span data-stu-id="83487-134">2</span></span>

<span data-ttu-id="83487-135">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="83487-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="83487-136">**Échec non spécifié**</span><span class="sxs-lookup"><span data-stu-id="83487-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="83487-137">8</span><span class="sxs-lookup"><span data-stu-id="83487-137">8</span></span>

<span data-ttu-id="83487-138">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="83487-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="83487-139">**Objet non valide**</span><span class="sxs-lookup"><span data-stu-id="83487-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="83487-140">9</span><span class="sxs-lookup"><span data-stu-id="83487-140">9</span></span>

<span data-ttu-id="83487-141">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="83487-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="83487-142">**L’objet existe déjà**</span><span class="sxs-lookup"><span data-stu-id="83487-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="83487-143">10</span><span class="sxs-lookup"><span data-stu-id="83487-143">10</span></span>

<span data-ttu-id="83487-144">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="83487-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="83487-145">**Système de fichiers non NTFS**</span><span class="sxs-lookup"><span data-stu-id="83487-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="83487-146">11</span><span class="sxs-lookup"><span data-stu-id="83487-146">11</span></span>

<span data-ttu-id="83487-147">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="83487-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="83487-148">**Plateforme non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="83487-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="83487-149">12</span><span class="sxs-lookup"><span data-stu-id="83487-149">12</span></span>

<span data-ttu-id="83487-150">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="83487-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="83487-151">**Le lecteur n’est pas le même**</span><span class="sxs-lookup"><span data-stu-id="83487-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="83487-152">13</span><span class="sxs-lookup"><span data-stu-id="83487-152">13</span></span>

<span data-ttu-id="83487-153">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="83487-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="83487-154">**Répertoire non vide**</span><span class="sxs-lookup"><span data-stu-id="83487-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="83487-155">14</span><span class="sxs-lookup"><span data-stu-id="83487-155">14</span></span>

<span data-ttu-id="83487-156">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="83487-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="83487-157">**Violation de partage**</span><span class="sxs-lookup"><span data-stu-id="83487-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="83487-158">15</span><span class="sxs-lookup"><span data-stu-id="83487-158">15</span></span>

<span data-ttu-id="83487-159">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="83487-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="83487-160">**Fichier de démarrage non valide**</span><span class="sxs-lookup"><span data-stu-id="83487-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="83487-161">16</span><span class="sxs-lookup"><span data-stu-id="83487-161">16</span></span>

<span data-ttu-id="83487-162">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="83487-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="83487-163">**Privilège non détenu**</span><span class="sxs-lookup"><span data-stu-id="83487-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="83487-164">17</span><span class="sxs-lookup"><span data-stu-id="83487-164">17</span></span>

<span data-ttu-id="83487-165">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="83487-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="83487-166">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="83487-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="83487-167">21</span><span class="sxs-lookup"><span data-stu-id="83487-167">21</span></span>

<span data-ttu-id="83487-168">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="83487-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83487-169">Notes</span><span class="sxs-lookup"><span data-stu-id="83487-169">Remarks</span></span>

<span data-ttu-id="83487-170">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="83487-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="83487-171">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="83487-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="83487-172">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="83487-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="83487-173">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="83487-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="83487-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83487-174">Requirements</span></span>



| <span data-ttu-id="83487-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83487-175">Requirement</span></span> | <span data-ttu-id="83487-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="83487-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83487-177">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83487-177">Minimum supported client</span></span><br/> | <span data-ttu-id="83487-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83487-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83487-179">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83487-179">Minimum supported server</span></span><br/> | <span data-ttu-id="83487-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83487-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83487-181">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83487-181">Namespace</span></span><br/>                | <span data-ttu-id="83487-182">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="83487-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83487-183">MOF</span><span class="sxs-lookup"><span data-stu-id="83487-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83487-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83487-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83487-185">DLL</span><span class="sxs-lookup"><span data-stu-id="83487-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83487-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83487-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83487-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83487-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83487-188">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="83487-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="83487-189">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="83487-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

