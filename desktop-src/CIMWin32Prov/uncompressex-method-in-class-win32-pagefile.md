---
description: Décompresse le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress.
ms.assetid: d4cfa42e-7f05-4d12-b629-14195fc04e77
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 158efe4d2390762433d66d170b774838c9e534d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111382"
---
# <a name="uncompressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="4efa1-104">Méthode UncompressEx de la \_ classe du fichier d’échange Win32</span><span class="sxs-lookup"><span data-stu-id="4efa1-104">UncompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="4efa1-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** décompresse le fichier d’échange logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4efa1-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="4efa1-106">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="4efa1-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="4efa1-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4efa1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4efa1-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4efa1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4efa1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4efa1-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4efa1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4efa1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4efa1-111">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4efa1-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-112">Nom du fichier ou du répertoire dans lequel la méthode **UncompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="4efa1-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="4efa1-113">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="4efa1-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-114">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4efa1-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-115">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="4efa1-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="4efa1-116">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="4efa1-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4efa1-117">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="4efa1-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-118">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4efa1-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-119">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="4efa1-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="4efa1-120">Pour les instances de fichier, le paramètre *recursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="4efa1-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4efa1-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4efa1-121">Return value</span></span>

<span data-ttu-id="4efa1-122">Retourne la valeur 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4efa1-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4efa1-123">**0**</span><span class="sxs-lookup"><span data-stu-id="4efa1-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-124">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="4efa1-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-125">**2**</span><span class="sxs-lookup"><span data-stu-id="4efa1-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-126">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="4efa1-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-127">**8**</span><span class="sxs-lookup"><span data-stu-id="4efa1-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-128">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4efa1-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-129">**9**</span><span class="sxs-lookup"><span data-stu-id="4efa1-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-130">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4efa1-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-131">**10**</span><span class="sxs-lookup"><span data-stu-id="4efa1-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-132">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4efa1-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-133">**11**</span><span class="sxs-lookup"><span data-stu-id="4efa1-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-134">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="4efa1-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-135">**12**</span><span class="sxs-lookup"><span data-stu-id="4efa1-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-136">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="4efa1-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-137">**13**</span><span class="sxs-lookup"><span data-stu-id="4efa1-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-138">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="4efa1-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-139">**14**</span><span class="sxs-lookup"><span data-stu-id="4efa1-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-140">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="4efa1-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-141">**15**</span><span class="sxs-lookup"><span data-stu-id="4efa1-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-142">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4efa1-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-143">**16**</span><span class="sxs-lookup"><span data-stu-id="4efa1-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-144">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4efa1-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-145">**17**</span><span class="sxs-lookup"><span data-stu-id="4efa1-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-146">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="4efa1-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="4efa1-147">**21**</span><span class="sxs-lookup"><span data-stu-id="4efa1-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4efa1-148">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4efa1-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4efa1-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4efa1-149">Requirements</span></span>



| <span data-ttu-id="4efa1-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4efa1-150">Requirement</span></span> | <span data-ttu-id="4efa1-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="4efa1-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4efa1-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efa1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4efa1-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4efa1-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4efa1-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efa1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4efa1-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4efa1-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4efa1-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4efa1-156">Namespace</span></span><br/>                | <span data-ttu-id="4efa1-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4efa1-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4efa1-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4efa1-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4efa1-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4efa1-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4efa1-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4efa1-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4efa1-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4efa1-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4efa1-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4efa1-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="4efa1-163">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4efa1-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4efa1-164">**\_Fichier d’échange Win32**</span><span class="sxs-lookup"><span data-stu-id="4efa1-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

