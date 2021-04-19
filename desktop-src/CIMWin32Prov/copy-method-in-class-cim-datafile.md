---
description: La méthode Copy copie le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Méthode Copy de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514750"
---
# <a name="copy-method-of-the-cim_datafile-class"></a><span data-ttu-id="717f0-103">Méthode Copy de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="717f0-103">Copy method of the CIM\_DataFile class</span></span>

<span data-ttu-id="717f0-104">La méthode **Copy** copie le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="717f0-104">The **Copy** method copies the logical file (or directory) that is specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="717f0-105">Une copie n’est pas prise en charge si elle nécessite le remplacement d’un fichier logique existant.</span><span class="sxs-lookup"><span data-stu-id="717f0-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="717f0-106">Cette méthode est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="717f0-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="717f0-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="717f0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="717f0-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="717f0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="717f0-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="717f0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="717f0-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="717f0-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="717f0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="717f0-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="717f0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="717f0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="717f0-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="717f0-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="717f0-114">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="717f0-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="717f0-115">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="717f0-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="717f0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="717f0-116">Return value</span></span>

<span data-ttu-id="717f0-117">Retourne la valeur 0 en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="717f0-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="717f0-118">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="717f0-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="717f0-119">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="717f0-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="717f0-120">**0**</span><span class="sxs-lookup"><span data-stu-id="717f0-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="717f0-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-122">**2**</span><span class="sxs-lookup"><span data-stu-id="717f0-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-123">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="717f0-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-124">**8**</span><span class="sxs-lookup"><span data-stu-id="717f0-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-125">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="717f0-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-126">**9**</span><span class="sxs-lookup"><span data-stu-id="717f0-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-127">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="717f0-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-128">**10**</span><span class="sxs-lookup"><span data-stu-id="717f0-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-129">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="717f0-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-130">**11**</span><span class="sxs-lookup"><span data-stu-id="717f0-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-131">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="717f0-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-132">**12**</span><span class="sxs-lookup"><span data-stu-id="717f0-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-133">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="717f0-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-134">**13**</span><span class="sxs-lookup"><span data-stu-id="717f0-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-135">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="717f0-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-136">**14**</span><span class="sxs-lookup"><span data-stu-id="717f0-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-137">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="717f0-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-138">**15**</span><span class="sxs-lookup"><span data-stu-id="717f0-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-139">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="717f0-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-140">**16**</span><span class="sxs-lookup"><span data-stu-id="717f0-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-141">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="717f0-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-142">**17**</span><span class="sxs-lookup"><span data-stu-id="717f0-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-143">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="717f0-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="717f0-144">**21**</span><span class="sxs-lookup"><span data-stu-id="717f0-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="717f0-145">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="717f0-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="717f0-146">Notes</span><span class="sxs-lookup"><span data-stu-id="717f0-146">Remarks</span></span>

<span data-ttu-id="717f0-147">La méthode de **copie** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="717f0-147">The **Copy** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="717f0-148">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="717f0-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="717f0-149">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="717f0-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="717f0-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="717f0-150">Requirements</span></span>



| <span data-ttu-id="717f0-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="717f0-151">Requirement</span></span> | <span data-ttu-id="717f0-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="717f0-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="717f0-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="717f0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="717f0-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="717f0-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="717f0-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="717f0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="717f0-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="717f0-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="717f0-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="717f0-157">Namespace</span></span><br/>                | <span data-ttu-id="717f0-158">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="717f0-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="717f0-159">MOF</span><span class="sxs-lookup"><span data-stu-id="717f0-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="717f0-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="717f0-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="717f0-161">DLL</span><span class="sxs-lookup"><span data-stu-id="717f0-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="717f0-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="717f0-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="717f0-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="717f0-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717f0-164">\_Fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="717f0-164">CIM\_DataFile</span></span>](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="717f0-165">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="717f0-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="717f0-166">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="717f0-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="717f0-167">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="717f0-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

