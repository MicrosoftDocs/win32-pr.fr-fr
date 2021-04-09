---
description: Décompresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode decompress.
ms.assetid: cd18d8b7-ab63-475c-a3a6-79611c9e032d
ms.tgt_platform: multiple
title: Méthode UncompressEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd02d0757745199249d64fa08d73f8b5ec65a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111386"
---
# <a name="uncompressex-method-of-the-win32_directory-class"></a><span data-ttu-id="15c78-104">Méthode UncompressEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="15c78-104">UncompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="15c78-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** décompresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="15c78-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="15c78-106">Cette méthode est une version étendue de la méthode [**decompress**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="15c78-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="15c78-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="15c78-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="15c78-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="15c78-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="15c78-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15c78-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="15c78-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15c78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c78-111">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="15c78-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c78-112">Nom du fichier/répertoire dans lequel la méthode **UncompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="15c78-112">Name of the file/directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="15c78-113">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="15c78-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-114">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="15c78-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15c78-115">Nomme le fichier/répertoire enfant à utiliser comme point de départ pour **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="15c78-115">Names the child file/directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="15c78-116">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="15c78-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="15c78-117">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="15c78-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

<span data-ttu-id="15c78-118">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="15c78-118">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-119">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="15c78-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15c78-120">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="15c78-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="15c78-121">Remarque : pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="15c78-121">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c78-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15c78-122">Return value</span></span>

<span data-ttu-id="15c78-123">Retourne la valeur 0 (zéro) si le fichier a été décompressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="15c78-123">Returns an value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="15c78-124">**0**</span><span class="sxs-lookup"><span data-stu-id="15c78-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-125">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="15c78-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-126">**2**</span><span class="sxs-lookup"><span data-stu-id="15c78-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-127">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="15c78-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-128">**8**</span><span class="sxs-lookup"><span data-stu-id="15c78-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-129">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="15c78-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-130">**9**</span><span class="sxs-lookup"><span data-stu-id="15c78-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-131">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="15c78-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-132">**10**</span><span class="sxs-lookup"><span data-stu-id="15c78-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-133">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="15c78-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-134">**11**</span><span class="sxs-lookup"><span data-stu-id="15c78-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-135">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="15c78-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-136">**12**</span><span class="sxs-lookup"><span data-stu-id="15c78-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-137">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="15c78-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-138">**13**</span><span class="sxs-lookup"><span data-stu-id="15c78-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="15c78-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-140">**14**</span><span class="sxs-lookup"><span data-stu-id="15c78-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-141">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="15c78-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-142">**15**</span><span class="sxs-lookup"><span data-stu-id="15c78-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-143">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="15c78-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-144">**16**</span><span class="sxs-lookup"><span data-stu-id="15c78-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-145">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="15c78-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-146">**17**</span><span class="sxs-lookup"><span data-stu-id="15c78-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-147">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="15c78-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="15c78-148">**21**</span><span class="sxs-lookup"><span data-stu-id="15c78-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="15c78-149">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="15c78-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15c78-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15c78-150">Requirements</span></span>



| <span data-ttu-id="15c78-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15c78-151">Requirement</span></span> | <span data-ttu-id="15c78-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="15c78-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c78-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15c78-153">Minimum supported client</span></span><br/> | <span data-ttu-id="15c78-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15c78-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15c78-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15c78-155">Minimum supported server</span></span><br/> | <span data-ttu-id="15c78-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15c78-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15c78-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="15c78-157">Namespace</span></span><br/>                | <span data-ttu-id="15c78-158">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="15c78-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15c78-159">MOF</span><span class="sxs-lookup"><span data-stu-id="15c78-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15c78-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15c78-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15c78-161">DLL</span><span class="sxs-lookup"><span data-stu-id="15c78-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c78-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c78-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c78-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15c78-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="15c78-164">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15c78-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="15c78-165">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="15c78-165">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

