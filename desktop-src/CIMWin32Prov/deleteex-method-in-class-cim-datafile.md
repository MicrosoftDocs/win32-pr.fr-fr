---
description: La méthode DeleteEx supprime le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode Delete et est héritée de la \_ LOGICALFILE CIM.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Méthode DeleteEx de la classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110522"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="60a7c-104">Méthode DeleteEx de la \_ classe de fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="60a7c-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="60a7c-105">La méthode **DeleteEx** supprime le fichier logique (ou le répertoire) qui est spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="60a7c-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="60a7c-106">Cette méthode est une version étendue de la méthode [**Delete**](delete-method-in-class-cim-datafile.md) et est héritée de la [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="60a7c-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60a7c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="60a7c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60a7c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60a7c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60a7c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="60a7c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60a7c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="60a7c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60a7c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60a7c-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="60a7c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60a7c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a7c-113">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60a7c-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60a7c-114">Chaîne qui représente le nom du fichier (ou répertoire) dans lequel la méthode a échoué.</span><span class="sxs-lookup"><span data-stu-id="60a7c-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="60a7c-115">Ce paramètre a la valeur null si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="60a7c-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="60a7c-116">*StartFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60a7c-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a7c-117">Chaîne qui représente le fichier enfant (ou le répertoire) à utiliser comme point de départ pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="60a7c-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="60a7c-118">En règle générale, le paramètre *StartFileName* est le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="60a7c-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="60a7c-119">Si ce paramètre a la valeur null, l’opération est effectuée sur le fichier (ou le répertoire) spécifié dans l’appel de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="60a7c-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a7c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60a7c-120">Return value</span></span>

<span data-ttu-id="60a7c-121">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="60a7c-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="60a7c-122">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="60a7c-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="60a7c-123">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="60a7c-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-124">0</span><span class="sxs-lookup"><span data-stu-id="60a7c-124">0</span></span>

<span data-ttu-id="60a7c-125">Réussite.</span><span class="sxs-lookup"><span data-stu-id="60a7c-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-126">2</span><span class="sxs-lookup"><span data-stu-id="60a7c-126">2</span></span>

<span data-ttu-id="60a7c-127">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="60a7c-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-128">8</span><span class="sxs-lookup"><span data-stu-id="60a7c-128">8</span></span>

<span data-ttu-id="60a7c-129">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="60a7c-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-130">9</span><span class="sxs-lookup"><span data-stu-id="60a7c-130">9</span></span>

<span data-ttu-id="60a7c-131">Objet non valide.</span><span class="sxs-lookup"><span data-stu-id="60a7c-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-132">10</span><span class="sxs-lookup"><span data-stu-id="60a7c-132">10</span></span>

<span data-ttu-id="60a7c-133">L’objet existe déjà.</span><span class="sxs-lookup"><span data-stu-id="60a7c-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-134">11</span><span class="sxs-lookup"><span data-stu-id="60a7c-134">11</span></span>

<span data-ttu-id="60a7c-135">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="60a7c-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-136">12</span><span class="sxs-lookup"><span data-stu-id="60a7c-136">12</span></span>

<span data-ttu-id="60a7c-137">Plateforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="60a7c-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-138">13</span><span class="sxs-lookup"><span data-stu-id="60a7c-138">13</span></span>

<span data-ttu-id="60a7c-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="60a7c-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-140">14</span><span class="sxs-lookup"><span data-stu-id="60a7c-140">14</span></span>

<span data-ttu-id="60a7c-141">le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="60a7c-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-142">15</span><span class="sxs-lookup"><span data-stu-id="60a7c-142">15</span></span>

<span data-ttu-id="60a7c-143">Violation de partage.</span><span class="sxs-lookup"><span data-stu-id="60a7c-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-144">16</span><span class="sxs-lookup"><span data-stu-id="60a7c-144">16</span></span>

<span data-ttu-id="60a7c-145">Fichier de démarrage non valide.</span><span class="sxs-lookup"><span data-stu-id="60a7c-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-146">17</span><span class="sxs-lookup"><span data-stu-id="60a7c-146">17</span></span>

<span data-ttu-id="60a7c-147">Privilège non détenu.</span><span class="sxs-lookup"><span data-stu-id="60a7c-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60a7c-148">21</span><span class="sxs-lookup"><span data-stu-id="60a7c-148">21</span></span>

<span data-ttu-id="60a7c-149">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="60a7c-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60a7c-150">Notes</span><span class="sxs-lookup"><span data-stu-id="60a7c-150">Remarks</span></span>

<span data-ttu-id="60a7c-151">La méthode **DeleteEx** dans le [**fichier de \_ fichier CIM**](cim-datafile.md) est implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="60a7c-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="60a7c-152">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="60a7c-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60a7c-153">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="60a7c-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60a7c-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60a7c-154">Requirements</span></span>



| <span data-ttu-id="60a7c-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60a7c-155">Requirement</span></span> | <span data-ttu-id="60a7c-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="60a7c-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60a7c-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60a7c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="60a7c-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60a7c-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60a7c-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60a7c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="60a7c-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60a7c-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60a7c-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60a7c-161">Namespace</span></span><br/>                | <span data-ttu-id="60a7c-162">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="60a7c-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60a7c-163">MOF</span><span class="sxs-lookup"><span data-stu-id="60a7c-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60a7c-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60a7c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="60a7c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60a7c-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60a7c-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60a7c-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60a7c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a7c-168">\_Fichier de fichier CIM</span><span class="sxs-lookup"><span data-stu-id="60a7c-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="60a7c-169">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="60a7c-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="60a7c-170">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="60a7c-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="60a7c-171">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="60a7c-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

