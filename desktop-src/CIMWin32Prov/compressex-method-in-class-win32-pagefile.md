---
description: Compresse le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode Compress).
ms.assetid: ea99367b-4d5e-4cd2-aa89-d250d1161f8f
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2823d12fc474b5a5023890596a116062d94a045f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860713"
---
# <a name="compressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="84414-103">Méthode CompressEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="84414-103">CompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="84414-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compresse le fichier de pagination logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="84414-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="84414-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="84414-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="84414-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="84414-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="84414-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84414-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="84414-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84414-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84414-109">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84414-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84414-110">Nom du fichier ou du répertoire dans lequel la méthode **CompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="84414-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="84414-111">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="84414-111">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="84414-112">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="84414-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84414-113">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="84414-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="84414-114">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="84414-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="84414-115">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="84414-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="84414-116">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="84414-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84414-117">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="84414-117">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="84414-118">Pour les instances de fichier, le paramètre *recursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="84414-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84414-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84414-119">Return value</span></span>

<span data-ttu-id="84414-120">Retourne la valeur 0 (zéro) si le fichier a été compressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="84414-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="84414-121">**0**</span><span class="sxs-lookup"><span data-stu-id="84414-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="84414-122">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="84414-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="84414-123">**2**</span><span class="sxs-lookup"><span data-stu-id="84414-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="84414-124">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="84414-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="84414-125">**8**</span><span class="sxs-lookup"><span data-stu-id="84414-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="84414-126">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="84414-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="84414-127">**9**</span><span class="sxs-lookup"><span data-stu-id="84414-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="84414-128">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="84414-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="84414-129">**10**</span><span class="sxs-lookup"><span data-stu-id="84414-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="84414-130">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="84414-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="84414-131">**11**</span><span class="sxs-lookup"><span data-stu-id="84414-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="84414-132">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="84414-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="84414-133">**12**</span><span class="sxs-lookup"><span data-stu-id="84414-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="84414-134">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="84414-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="84414-135">**13**</span><span class="sxs-lookup"><span data-stu-id="84414-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="84414-136">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="84414-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="84414-137">**14**</span><span class="sxs-lookup"><span data-stu-id="84414-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="84414-138">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="84414-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="84414-139">**15**</span><span class="sxs-lookup"><span data-stu-id="84414-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="84414-140">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="84414-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="84414-141">**16**</span><span class="sxs-lookup"><span data-stu-id="84414-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="84414-142">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="84414-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="84414-143">**17**</span><span class="sxs-lookup"><span data-stu-id="84414-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="84414-144">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="84414-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="84414-145">**21**</span><span class="sxs-lookup"><span data-stu-id="84414-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="84414-146">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="84414-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84414-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84414-147">Requirements</span></span>



| <span data-ttu-id="84414-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84414-148">Requirement</span></span> | <span data-ttu-id="84414-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="84414-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84414-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84414-150">Minimum supported client</span></span><br/> | <span data-ttu-id="84414-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84414-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84414-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84414-152">Minimum supported server</span></span><br/> | <span data-ttu-id="84414-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84414-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84414-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84414-154">Namespace</span></span><br/>                | <span data-ttu-id="84414-155">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="84414-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84414-156">MOF</span><span class="sxs-lookup"><span data-stu-id="84414-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84414-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84414-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84414-158">DLL</span><span class="sxs-lookup"><span data-stu-id="84414-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84414-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84414-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84414-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84414-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="84414-161">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84414-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84414-162">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="84414-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

