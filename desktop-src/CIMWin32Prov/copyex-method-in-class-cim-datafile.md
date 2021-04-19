---
description: La méthode CopyEx copie le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515786"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="dba84-103">Méthode CopyEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="dba84-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="dba84-104">La méthode **CopyEx** copie le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="dba84-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="dba84-105">Une copie n’est pas prise en charge si elle nécessite le remplacement d’un fichier logique existant.</span><span class="sxs-lookup"><span data-stu-id="dba84-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="dba84-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-cim-datafile.md) et est héritée de la [ \_ LogicalFile CIM](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="dba84-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dba84-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="dba84-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dba84-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dba84-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dba84-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="dba84-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dba84-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dba84-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dba84-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dba84-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="dba84-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dba84-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba84-113">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dba84-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba84-114">Nom complet du fichier de destination (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="dba84-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="dba84-115">Exemple : « c : \\ temp \\ newDirectory »</span><span class="sxs-lookup"><span data-stu-id="dba84-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="dba84-116">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dba84-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dba84-117">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="dba84-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="dba84-118">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="dba84-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="dba84-119">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dba84-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba84-120">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="dba84-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="dba84-121">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier (ou le répertoire) auquel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="dba84-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="dba84-122">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="dba84-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="dba84-123">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="dba84-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="dba84-124">*Récursif* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dba84-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba84-125">Si la valeur est TRUE, la méthode est également appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance du [**\_ fichier de fichier CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="dba84-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="dba84-126">Pour les instances de fichier, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="dba84-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba84-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dba84-127">Return value</span></span>

<span data-ttu-id="dba84-128">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="dba84-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="dba84-129">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="dba84-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="dba84-130">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="dba84-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="dba84-131">0</span><span class="sxs-lookup"><span data-stu-id="dba84-131">0</span></span>

<span data-ttu-id="dba84-132">Réussite.</span><span class="sxs-lookup"><span data-stu-id="dba84-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-133">2</span><span class="sxs-lookup"><span data-stu-id="dba84-133">2</span></span>

<span data-ttu-id="dba84-134">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="dba84-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-135">8</span><span class="sxs-lookup"><span data-stu-id="dba84-135">8</span></span>

<span data-ttu-id="dba84-136">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="dba84-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-137">9</span><span class="sxs-lookup"><span data-stu-id="dba84-137">9</span></span>

<span data-ttu-id="dba84-138">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="dba84-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-139">10</span><span class="sxs-lookup"><span data-stu-id="dba84-139">10</span></span>

<span data-ttu-id="dba84-140">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="dba84-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-141">11</span><span class="sxs-lookup"><span data-stu-id="dba84-141">11</span></span>

<span data-ttu-id="dba84-142">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="dba84-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-143">12</span><span class="sxs-lookup"><span data-stu-id="dba84-143">12</span></span>

<span data-ttu-id="dba84-144">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="dba84-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-145">13</span><span class="sxs-lookup"><span data-stu-id="dba84-145">13</span></span>

<span data-ttu-id="dba84-146">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="dba84-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-147">14</span><span class="sxs-lookup"><span data-stu-id="dba84-147">14</span></span>

<span data-ttu-id="dba84-148">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="dba84-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-149">15</span><span class="sxs-lookup"><span data-stu-id="dba84-149">15</span></span>

<span data-ttu-id="dba84-150">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="dba84-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-151">16</span><span class="sxs-lookup"><span data-stu-id="dba84-151">16</span></span>

<span data-ttu-id="dba84-152">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="dba84-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-153">17</span><span class="sxs-lookup"><span data-stu-id="dba84-153">17</span></span>

<span data-ttu-id="dba84-154">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="dba84-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="dba84-155">21</span><span class="sxs-lookup"><span data-stu-id="dba84-155">21</span></span>

<span data-ttu-id="dba84-156">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="dba84-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dba84-157">Notes</span><span class="sxs-lookup"><span data-stu-id="dba84-157">Remarks</span></span>

<span data-ttu-id="dba84-158">La méthode **CopyEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="dba84-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="dba84-159">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="dba84-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dba84-160">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="dba84-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba84-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dba84-161">Requirements</span></span>



| <span data-ttu-id="dba84-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dba84-162">Requirement</span></span> | <span data-ttu-id="dba84-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="dba84-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dba84-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dba84-164">Minimum supported client</span></span><br/> | <span data-ttu-id="dba84-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dba84-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dba84-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dba84-166">Minimum supported server</span></span><br/> | <span data-ttu-id="dba84-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dba84-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dba84-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dba84-168">Namespace</span></span><br/>                | <span data-ttu-id="dba84-169">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="dba84-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dba84-170">MOF</span><span class="sxs-lookup"><span data-stu-id="dba84-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dba84-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dba84-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dba84-172">DLL</span><span class="sxs-lookup"><span data-stu-id="dba84-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dba84-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dba84-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dba84-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dba84-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba84-175">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="dba84-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="dba84-176">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="dba84-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="dba84-177">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="dba84-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

