---
description: Obtient la propriété du fichier de données logiques qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip et est héritée de CIM \_ LogicalFile.
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41124567e8743227f46c9cb3b84dcb0d1f788bc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483720"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a><span data-ttu-id="cf622-104">Méthode TakeOwnerShipEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="cf622-104">TakeOwnerShipEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="cf622-105">La méthode **TakeOwnerShipEx** obtient la propriété du fichier de données logiques qui est spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cf622-105">The **TakeOwnerShipEx** method obtains ownership of the logical data file that is specified in the object path.</span></span> <span data-ttu-id="cf622-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-cim-datafile.md) et est héritée de [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="cf622-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="cf622-107">Si le fichier logique est un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="cf622-107">If the logical file is a directory, then this method will act recursively, taking ownership of all files and subdirectories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf622-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="cf622-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf622-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf622-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf622-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="cf622-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf622-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf622-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf622-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf622-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="cf622-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf622-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf622-114">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cf622-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf622-115">Nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="cf622-115">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="cf622-116">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="cf622-116">This parameter will be null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-117">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf622-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf622-118">Fichier enfant (ou répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cf622-118">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="cf622-119">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="cf622-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="cf622-120">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="cf622-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="cf622-121">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="cf622-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-122">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf622-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf622-123">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du fichier de [**\_ fichier CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="cf622-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="cf622-124">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="cf622-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf622-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf622-125">Return value</span></span>

<span data-ttu-id="cf622-126">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="cf622-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="cf622-127">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cf622-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cf622-128">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cf622-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cf622-129">**0**</span><span class="sxs-lookup"><span data-stu-id="cf622-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-130">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cf622-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-131">**2**</span><span class="sxs-lookup"><span data-stu-id="cf622-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-132">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="cf622-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-133">**8**</span><span class="sxs-lookup"><span data-stu-id="cf622-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-134">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="cf622-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-135">**9**</span><span class="sxs-lookup"><span data-stu-id="cf622-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-136">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="cf622-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-137">**10**</span><span class="sxs-lookup"><span data-stu-id="cf622-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-138">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="cf622-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-139">**11**</span><span class="sxs-lookup"><span data-stu-id="cf622-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-140">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="cf622-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-141">**12**</span><span class="sxs-lookup"><span data-stu-id="cf622-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-142">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="cf622-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-143">**13**</span><span class="sxs-lookup"><span data-stu-id="cf622-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-144">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="cf622-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-145">**14**</span><span class="sxs-lookup"><span data-stu-id="cf622-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-146">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="cf622-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-147">**15**</span><span class="sxs-lookup"><span data-stu-id="cf622-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-148">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="cf622-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-149">**16**</span><span class="sxs-lookup"><span data-stu-id="cf622-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-150">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="cf622-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-151">**17**</span><span class="sxs-lookup"><span data-stu-id="cf622-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-152">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="cf622-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="cf622-153">**21**</span><span class="sxs-lookup"><span data-stu-id="cf622-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="cf622-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="cf622-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf622-155">Notes</span><span class="sxs-lookup"><span data-stu-id="cf622-155">Remarks</span></span>

<span data-ttu-id="cf622-156">La méthode **TakeOwnerShipEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="cf622-156">The **TakeOwnerShipEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="cf622-157">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf622-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf622-158">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cf622-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf622-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf622-159">Requirements</span></span>



| <span data-ttu-id="cf622-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf622-160">Requirement</span></span> | <span data-ttu-id="cf622-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf622-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf622-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf622-162">Minimum supported client</span></span><br/> | <span data-ttu-id="cf622-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf622-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf622-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf622-164">Minimum supported server</span></span><br/> | <span data-ttu-id="cf622-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf622-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf622-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf622-166">Namespace</span></span><br/>                | <span data-ttu-id="cf622-167">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="cf622-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf622-168">MOF</span><span class="sxs-lookup"><span data-stu-id="cf622-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf622-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf622-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf622-170">DLL</span><span class="sxs-lookup"><span data-stu-id="cf622-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf622-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf622-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf622-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf622-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf622-173">\_Fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="cf622-173">CIM\_DataFile</span></span>](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="cf622-174">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="cf622-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="cf622-175">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="cf622-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="cf622-176">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="cf622-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

