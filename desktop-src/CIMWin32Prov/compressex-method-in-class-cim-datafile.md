---
description: Utilise la compression NTFS pour compresser le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 070a15a0fb134c92e7c436e071e09b7cc09fa5dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200897"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="4a5b8-104">Méthode CompressEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="4a5b8-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="4a5b8-105">La méthode **CompressEx** utilise la compression NTFS pour compresser le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="4a5b8-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="4a5b8-107">Cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-cim-datafile.md) et est héritée de la [ \_ LogicalFile CIM](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a5b8-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a5b8-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a5b8-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4a5b8-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5b8-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a5b8-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4a5b8-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a5b8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a5b8-114">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-115">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4a5b8-116">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-117">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-118">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="4a5b8-119">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* qui spécifie le fichier ou le répertoire auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4a5b8-120">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="4a5b8-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="4a5b8-121">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-122">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a5b8-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-123">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du fichier de [**\_ fichier CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="4a5b8-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="4a5b8-124">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a5b8-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a5b8-125">Return value</span></span>

<span data-ttu-id="4a5b8-126">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="4a5b8-127">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4a5b8-128">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4a5b8-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4a5b8-129">**0**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-130">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-131">**2**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-132">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-133">**8**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-134">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-135">**9**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-136">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-137">**10**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-138">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-139">**11**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-140">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-141">**12**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-142">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-143">**13**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-144">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-145">**14**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-146">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-147">**15**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-148">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-149">**16**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-150">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-151">**17**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-152">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4a5b8-153">**21**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4a5b8-154">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a5b8-155">Notes</span><span class="sxs-lookup"><span data-stu-id="4a5b8-155">Remarks</span></span>

<span data-ttu-id="4a5b8-156">La méthode **CompressEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="4a5b8-157">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a5b8-158">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4a5b8-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a5b8-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a5b8-159">Requirements</span></span>



| <span data-ttu-id="4a5b8-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a5b8-160">Requirement</span></span> | <span data-ttu-id="4a5b8-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a5b8-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5b8-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a5b8-162">Minimum supported client</span></span><br/> | <span data-ttu-id="4a5b8-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a5b8-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a5b8-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a5b8-164">Minimum supported server</span></span><br/> | <span data-ttu-id="4a5b8-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a5b8-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a5b8-166">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4a5b8-166">Namespace</span></span><br/>                | <span data-ttu-id="4a5b8-167">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4a5b8-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a5b8-168">MOF</span><span class="sxs-lookup"><span data-stu-id="4a5b8-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a5b8-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a5b8-170">DLL</span><span class="sxs-lookup"><span data-stu-id="4a5b8-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a5b8-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a5b8-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a5b8-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a5b8-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5b8-173">\_Fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="4a5b8-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="4a5b8-174">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="4a5b8-175">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="4a5b8-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="4a5b8-176">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="4a5b8-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

