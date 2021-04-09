---
description: Décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111394"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="b931c-104">Méthode UncompressEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="b931c-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b931c-105">La méthode **UncompressEx** décompresse le fichier de données logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b931c-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="b931c-106">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-cim-datafile.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b931c-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b931c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="b931c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b931c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b931c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b931c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b931c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b931c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b931c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b931c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b931c-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b931c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b931c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b931c-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b931c-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b931c-114">Nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="b931c-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="b931c-115">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="b931c-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-116">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b931c-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b931c-117">Fichier enfant (ou répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b931c-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="b931c-118">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="b931c-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b931c-119">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="b931c-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="b931c-120">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="b931c-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-121">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b931c-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b931c-122">Si la **valeur est true**, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du fichier de [**\_ fichier CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="b931c-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="b931c-123">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b931c-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b931c-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b931c-124">Return value</span></span>

<span data-ttu-id="b931c-125">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b931c-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b931c-126">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b931c-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b931c-127">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b931c-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b931c-128">**0**</span><span class="sxs-lookup"><span data-stu-id="b931c-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-129">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b931c-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-130">**2**</span><span class="sxs-lookup"><span data-stu-id="b931c-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-131">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b931c-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-132">**8**</span><span class="sxs-lookup"><span data-stu-id="b931c-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-133">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="b931c-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-134">**9**</span><span class="sxs-lookup"><span data-stu-id="b931c-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-135">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="b931c-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-136">**10**</span><span class="sxs-lookup"><span data-stu-id="b931c-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-137">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b931c-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-138">**11**</span><span class="sxs-lookup"><span data-stu-id="b931c-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-139">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="b931c-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-140">**12**</span><span class="sxs-lookup"><span data-stu-id="b931c-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-141">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="b931c-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-142">**13**</span><span class="sxs-lookup"><span data-stu-id="b931c-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-143">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="b931c-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-144">**14**</span><span class="sxs-lookup"><span data-stu-id="b931c-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-145">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="b931c-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-146">**15**</span><span class="sxs-lookup"><span data-stu-id="b931c-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-147">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="b931c-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-148">**16**</span><span class="sxs-lookup"><span data-stu-id="b931c-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-149">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="b931c-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-150">**17**</span><span class="sxs-lookup"><span data-stu-id="b931c-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-151">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="b931c-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b931c-152">**21**</span><span class="sxs-lookup"><span data-stu-id="b931c-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b931c-153">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="b931c-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b931c-154">Notes</span><span class="sxs-lookup"><span data-stu-id="b931c-154">Remarks</span></span>

<span data-ttu-id="b931c-155">La méthode **UncompressEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="b931c-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b931c-156">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="b931c-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b931c-157">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b931c-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b931c-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b931c-158">Requirements</span></span>



| <span data-ttu-id="b931c-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b931c-159">Requirement</span></span> | <span data-ttu-id="b931c-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="b931c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b931c-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b931c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b931c-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b931c-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b931c-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b931c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b931c-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b931c-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b931c-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b931c-165">Namespace</span></span><br/>                | <span data-ttu-id="b931c-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b931c-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b931c-167">MOF</span><span class="sxs-lookup"><span data-stu-id="b931c-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b931c-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b931c-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b931c-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b931c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b931c-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b931c-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b931c-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b931c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b931c-172">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="b931c-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b931c-173">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="b931c-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b931c-174">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="b931c-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b931c-175">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="b931c-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

