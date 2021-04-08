---
description: Copie le fichier de pagination logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre FileName. Cette méthode est une version étendue de la méthode de copie.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: Méthode CopyEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861754"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="8f710-104">Méthode CopyEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="8f710-104">CopyEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="8f710-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copie le fichier de pagination logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="8f710-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="8f710-106">Cette méthode est une version étendue de la méthode de [**copie**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="8f710-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="8f710-107">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8f710-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="8f710-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8f710-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f710-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f710-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f710-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f710-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8f710-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f710-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f710-112">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8f710-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f710-113">Nom complet de la copie du fichier (ou du répertoire).</span><span class="sxs-lookup"><span data-stu-id="8f710-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="8f710-114">Exemple : c : \\ temp \\ newDirectory</span><span class="sxs-lookup"><span data-stu-id="8f710-114">Example: c:\\temp\\newdirectory</span></span>

</dd> <dt>

<span data-ttu-id="8f710-115">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8f710-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f710-116">Nom du fichier ou du répertoire dans lequel la méthode **CopyEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="8f710-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="8f710-117">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="8f710-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-118">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8f710-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f710-119">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="8f710-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="8f710-120">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="8f710-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8f710-121">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="8f710-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-122">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8f710-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f710-123">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8f710-123">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="8f710-124">Pour les instances de fichier, le paramètre *recursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8f710-124">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f710-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f710-125">Return value</span></span>

<span data-ttu-id="8f710-126">Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8f710-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8f710-127">**0**</span><span class="sxs-lookup"><span data-stu-id="8f710-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-128">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="8f710-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-129">**2**</span><span class="sxs-lookup"><span data-stu-id="8f710-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-130">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="8f710-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-131">**8**</span><span class="sxs-lookup"><span data-stu-id="8f710-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-132">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8f710-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-133">**9**</span><span class="sxs-lookup"><span data-stu-id="8f710-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-134">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8f710-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-135">**10**</span><span class="sxs-lookup"><span data-stu-id="8f710-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-136">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8f710-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-137">**11**</span><span class="sxs-lookup"><span data-stu-id="8f710-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-138">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="8f710-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-139">**12**</span><span class="sxs-lookup"><span data-stu-id="8f710-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-140">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="8f710-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-141">**13**</span><span class="sxs-lookup"><span data-stu-id="8f710-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-142">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="8f710-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-143">**14**</span><span class="sxs-lookup"><span data-stu-id="8f710-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-144">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="8f710-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-145">**15**</span><span class="sxs-lookup"><span data-stu-id="8f710-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-146">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8f710-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-147">**16**</span><span class="sxs-lookup"><span data-stu-id="8f710-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-148">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8f710-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-149">**17**</span><span class="sxs-lookup"><span data-stu-id="8f710-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-150">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="8f710-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8f710-151">**21**</span><span class="sxs-lookup"><span data-stu-id="8f710-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8f710-152">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8f710-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f710-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f710-153">Requirements</span></span>



| <span data-ttu-id="8f710-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f710-154">Requirement</span></span> | <span data-ttu-id="8f710-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f710-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f710-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f710-156">Minimum supported client</span></span><br/> | <span data-ttu-id="8f710-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f710-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f710-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f710-158">Minimum supported server</span></span><br/> | <span data-ttu-id="8f710-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f710-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f710-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f710-160">Namespace</span></span><br/>                | <span data-ttu-id="8f710-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8f710-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f710-162">MOF</span><span class="sxs-lookup"><span data-stu-id="8f710-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f710-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f710-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f710-164">DLL</span><span class="sxs-lookup"><span data-stu-id="8f710-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f710-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f710-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f710-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f710-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f710-167">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f710-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8f710-168">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="8f710-168">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

