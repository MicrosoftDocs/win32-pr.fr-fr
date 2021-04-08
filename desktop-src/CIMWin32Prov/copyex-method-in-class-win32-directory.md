---
description: Copie le fichier d’entrée de répertoire logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName. Cette méthode est une version étendue de la méthode de copie.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861757"
---
# <a name="copyex-method-of-the-win32_directory-class"></a><span data-ttu-id="ef4dc-104">Méthode CopyEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="ef4dc-104">CopyEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="ef4dc-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copie le fichier ou le répertoire d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="ef4dc-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="ef4dc-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="ef4dc-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="ef4dc-107">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="ef4dc-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ef4dc-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef4dc-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef4dc-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4dc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef4dc-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ef4dc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef4dc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef4dc-112">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef4dc-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-113">Nom complet de la copie du fichier (ou du répertoire).</span><span class="sxs-lookup"><span data-stu-id="ef4dc-113">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="ef4dc-114">Exemple : c : \\ temp \\ newDirectory.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-114">Example: c:\\temp\\newdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-115">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef4dc-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-116">Nom du fichier ou du répertoire dans lequel la méthode **CopyEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="ef4dc-117">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-117">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-118">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ef4dc-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-119">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="ef4dc-120">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ef4dc-121">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="ef4dc-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="ef4dc-122">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-122">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-123">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ef4dc-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-124">Si la **valeur est true**, les fichiers et les répertoires sont copiés de manière récursive dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ef4dc-124">If **true**, files and directories will be copied recursively within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="ef4dc-125">Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-125">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef4dc-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef4dc-126">Return value</span></span>

<span data-ttu-id="ef4dc-127">Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-127">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ef4dc-128">**0**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-129">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-129">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-130">**2**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-131">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-131">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-132">**8**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-133">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-133">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-134">**9**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-135">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-135">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-136">**10**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-137">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-137">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-138">**11**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-139">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-139">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-140">**12**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-141">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-141">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-142">**13**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-143">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-143">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-144">**14**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-145">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-145">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-146">**15**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-147">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-147">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-148">**16**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-149">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-149">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-150">**17**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-151">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-151">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ef4dc-152">**21**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ef4dc-153">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ef4dc-153">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef4dc-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef4dc-154">Requirements</span></span>



| <span data-ttu-id="ef4dc-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef4dc-155">Requirement</span></span> | <span data-ttu-id="ef4dc-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef4dc-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4dc-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef4dc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ef4dc-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef4dc-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef4dc-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef4dc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ef4dc-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef4dc-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef4dc-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef4dc-161">Namespace</span></span><br/>                | <span data-ttu-id="ef4dc-162">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ef4dc-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef4dc-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ef4dc-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef4dc-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef4dc-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef4dc-165">DLL</span><span class="sxs-lookup"><span data-stu-id="ef4dc-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef4dc-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef4dc-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef4dc-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef4dc-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef4dc-168">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef4dc-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ef4dc-169">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="ef4dc-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

