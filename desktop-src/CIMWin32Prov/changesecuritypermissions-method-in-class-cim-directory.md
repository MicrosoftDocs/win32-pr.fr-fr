---
description: 'Méthode ChangeSecurityPermissions de la classe CIM_Directory : modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet.'
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Méthode ChangeSecurityPermissions de la classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091067"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="07c12-103">Méthode ChangeSecurityPermissions de la \_ classe de répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="07c12-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="07c12-104">La méthode **ChangeSecurityPermissions** modifie les autorisations de sécurité pour le fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="07c12-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="07c12-105">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en modifiant les autorisations de sécurité pour tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="07c12-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="07c12-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="07c12-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07c12-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="07c12-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="07c12-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="07c12-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="07c12-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="07c12-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07c12-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07c12-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07c12-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07c12-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="07c12-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07c12-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c12-113">*SecurityDescriptor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07c12-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c12-114">Spécifie des informations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="07c12-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="07c12-115">Une liste de contrôle d’accès (ACL) **null** dans la structure du [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) accorde un accès illimité.</span><span class="sxs-lookup"><span data-stu-id="07c12-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="07c12-116">*Option* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07c12-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07c12-117">Privilège de sécurité à modifier.</span><span class="sxs-lookup"><span data-stu-id="07c12-117">Security privilege to modify.</span></span> <span data-ttu-id="07c12-118">Par exemple, pour modifier la sécurité du propriétaire et de la liste DACL, utilisez :</span><span class="sxs-lookup"><span data-stu-id="07c12-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="07c12-119">ou</span><span class="sxs-lookup"><span data-stu-id="07c12-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="07c12-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité du propriétaire** (1)</span><span class="sxs-lookup"><span data-stu-id="07c12-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="07c12-121">Modifiez le propriétaire du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="07c12-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="07c12-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifier \_ \_ \_ Informations sur la sécurité du groupe** (2)</span><span class="sxs-lookup"><span data-stu-id="07c12-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="07c12-123">Modifiez le groupe du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="07c12-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="07c12-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="07c12-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="07c12-125">Modifiez la liste de contrôle d’accès du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="07c12-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="07c12-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifier \_ \_ \_ Informations de sécurité SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="07c12-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="07c12-127">Modifiez la liste de contrôle d’accès système du fichier logique.</span><span class="sxs-lookup"><span data-stu-id="07c12-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c12-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07c12-128">Return value</span></span>

<span data-ttu-id="07c12-129">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="07c12-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="07c12-130">0</span><span class="sxs-lookup"><span data-stu-id="07c12-130">0</span></span>

<span data-ttu-id="07c12-131">Réussite.</span><span class="sxs-lookup"><span data-stu-id="07c12-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-132">2</span><span class="sxs-lookup"><span data-stu-id="07c12-132">2</span></span>

<span data-ttu-id="07c12-133">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="07c12-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-134">8</span><span class="sxs-lookup"><span data-stu-id="07c12-134">8</span></span>

<span data-ttu-id="07c12-135">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="07c12-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-136">9</span><span class="sxs-lookup"><span data-stu-id="07c12-136">9</span></span>

<span data-ttu-id="07c12-137">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="07c12-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-138">10</span><span class="sxs-lookup"><span data-stu-id="07c12-138">10</span></span>

<span data-ttu-id="07c12-139">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="07c12-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-140">11</span><span class="sxs-lookup"><span data-stu-id="07c12-140">11</span></span>

<span data-ttu-id="07c12-141">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="07c12-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-142">12</span><span class="sxs-lookup"><span data-stu-id="07c12-142">12</span></span>

<span data-ttu-id="07c12-143">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="07c12-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-144">13</span><span class="sxs-lookup"><span data-stu-id="07c12-144">13</span></span>

<span data-ttu-id="07c12-145">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="07c12-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-146">14</span><span class="sxs-lookup"><span data-stu-id="07c12-146">14</span></span>

<span data-ttu-id="07c12-147">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="07c12-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-148">15</span><span class="sxs-lookup"><span data-stu-id="07c12-148">15</span></span>

<span data-ttu-id="07c12-149">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="07c12-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-150">16</span><span class="sxs-lookup"><span data-stu-id="07c12-150">16</span></span>

<span data-ttu-id="07c12-151">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="07c12-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-152">17</span><span class="sxs-lookup"><span data-stu-id="07c12-152">17</span></span>

<span data-ttu-id="07c12-153">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="07c12-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="07c12-154">21</span><span class="sxs-lookup"><span data-stu-id="07c12-154">21</span></span>

<span data-ttu-id="07c12-155">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="07c12-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07c12-156">Notes </span><span class="sxs-lookup"><span data-stu-id="07c12-156">Remarks</span></span>

<span data-ttu-id="07c12-157">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="07c12-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="07c12-158">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="07c12-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="07c12-159">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="07c12-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="07c12-160">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="07c12-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c12-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07c12-161">Requirements</span></span>



| <span data-ttu-id="07c12-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07c12-162">Requirement</span></span> | <span data-ttu-id="07c12-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="07c12-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07c12-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c12-164">Minimum supported client</span></span><br/> | <span data-ttu-id="07c12-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07c12-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07c12-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07c12-166">Minimum supported server</span></span><br/> | <span data-ttu-id="07c12-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07c12-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07c12-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="07c12-168">Namespace</span></span><br/>                | <span data-ttu-id="07c12-169">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="07c12-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07c12-170">MOF</span><span class="sxs-lookup"><span data-stu-id="07c12-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07c12-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07c12-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07c12-172">DLL</span><span class="sxs-lookup"><span data-stu-id="07c12-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c12-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c12-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c12-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07c12-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c12-175">\_Répertoire CIM</span><span class="sxs-lookup"><span data-stu-id="07c12-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="07c12-176">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="07c12-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

