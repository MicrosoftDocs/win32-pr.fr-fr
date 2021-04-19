---
description: Compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode Compress).
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Méthode CompressEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517178"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="39f71-103">Méthode CompressEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="39f71-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="39f71-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet (cette méthode est une version étendue de la méthode [**Compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="39f71-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="39f71-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="39f71-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="39f71-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="39f71-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="39f71-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f71-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="39f71-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39f71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39f71-109">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="39f71-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39f71-110">Nom du fichier ou du répertoire dans lequel la méthode **CompressEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="39f71-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="39f71-111">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="39f71-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-112">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="39f71-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39f71-113">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="39f71-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="39f71-114">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="39f71-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="39f71-115">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="39f71-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="39f71-116">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="39f71-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-117">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="39f71-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39f71-118">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="39f71-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="39f71-119">Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="39f71-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39f71-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39f71-120">Return value</span></span>

<span data-ttu-id="39f71-121">Retourne la valeur 0 (zéro) si le fichier a été compressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="39f71-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="39f71-122">**0**</span><span class="sxs-lookup"><span data-stu-id="39f71-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-123">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="39f71-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-124">**2**</span><span class="sxs-lookup"><span data-stu-id="39f71-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-125">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="39f71-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-126">**8**</span><span class="sxs-lookup"><span data-stu-id="39f71-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-127">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="39f71-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-128">**9**</span><span class="sxs-lookup"><span data-stu-id="39f71-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-129">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="39f71-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-130">**10**</span><span class="sxs-lookup"><span data-stu-id="39f71-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-131">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="39f71-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-132">**11**</span><span class="sxs-lookup"><span data-stu-id="39f71-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-133">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="39f71-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-134">**12**</span><span class="sxs-lookup"><span data-stu-id="39f71-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-135">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="39f71-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-136">**13**</span><span class="sxs-lookup"><span data-stu-id="39f71-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-137">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="39f71-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-138">**14**</span><span class="sxs-lookup"><span data-stu-id="39f71-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-139">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="39f71-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-140">**15**</span><span class="sxs-lookup"><span data-stu-id="39f71-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-141">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="39f71-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-142">**16**</span><span class="sxs-lookup"><span data-stu-id="39f71-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-143">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="39f71-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-144">**17**</span><span class="sxs-lookup"><span data-stu-id="39f71-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-145">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="39f71-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="39f71-146">**21**</span><span class="sxs-lookup"><span data-stu-id="39f71-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="39f71-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="39f71-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39f71-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39f71-148">Requirements</span></span>



| <span data-ttu-id="39f71-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39f71-149">Requirement</span></span> | <span data-ttu-id="39f71-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="39f71-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f71-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f71-151">Minimum supported client</span></span><br/> | <span data-ttu-id="39f71-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39f71-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39f71-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39f71-153">Minimum supported server</span></span><br/> | <span data-ttu-id="39f71-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39f71-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39f71-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39f71-155">Namespace</span></span><br/>                | <span data-ttu-id="39f71-156">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="39f71-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39f71-157">MOF</span><span class="sxs-lookup"><span data-stu-id="39f71-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39f71-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39f71-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39f71-159">DLL</span><span class="sxs-lookup"><span data-stu-id="39f71-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f71-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f71-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f71-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39f71-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="39f71-162">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39f71-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="39f71-163">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="39f71-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

