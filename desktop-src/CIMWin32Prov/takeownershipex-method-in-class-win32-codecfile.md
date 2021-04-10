---
description: Obtient la propriété du fichier de codec logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36512d48fe724da42c39c0d3d0686a706f54472d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847045"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="1d93a-104">Méthode TakeOwnerShipEx de la \_ classe Win32 CodecFile</span><span class="sxs-lookup"><span data-stu-id="1d93a-104">TakeOwnerShipEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="1d93a-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtient la propriété du fichier de codec logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1d93a-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical codec file specified in the object path.</span></span> <span data-ttu-id="1d93a-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="1d93a-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="1d93a-107">Si le fichier logique est effectivement un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="1d93a-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="1d93a-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1d93a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d93a-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d93a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d93a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d93a-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1d93a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d93a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d93a-112">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d93a-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-113">Nom du fichier ou du répertoire dans lequel la méthode **TakeOwnerShipEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="1d93a-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="1d93a-114">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="1d93a-114">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-115">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1d93a-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-116">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **TakeOwnerShipEx**. Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="1d93a-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1d93a-117">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="1d93a-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-118">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1d93a-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-119">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1d93a-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="1d93a-120">Remarque : pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1d93a-120">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d93a-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d93a-121">Return value</span></span>

<span data-ttu-id="1d93a-122">Retourne une valeur entière égale à 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1d93a-122">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1d93a-123">**0**</span><span class="sxs-lookup"><span data-stu-id="1d93a-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-124">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="1d93a-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-125">**2**</span><span class="sxs-lookup"><span data-stu-id="1d93a-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-126">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="1d93a-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-127">**8**</span><span class="sxs-lookup"><span data-stu-id="1d93a-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-128">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1d93a-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-129">**9**</span><span class="sxs-lookup"><span data-stu-id="1d93a-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-130">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1d93a-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-131">**10**</span><span class="sxs-lookup"><span data-stu-id="1d93a-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-132">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1d93a-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-133">**11**</span><span class="sxs-lookup"><span data-stu-id="1d93a-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-134">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="1d93a-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-135">**12**</span><span class="sxs-lookup"><span data-stu-id="1d93a-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-136">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="1d93a-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-137">**13**</span><span class="sxs-lookup"><span data-stu-id="1d93a-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-138">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="1d93a-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-139">**14**</span><span class="sxs-lookup"><span data-stu-id="1d93a-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-140">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="1d93a-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-141">**15**</span><span class="sxs-lookup"><span data-stu-id="1d93a-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-142">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1d93a-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-143">**16**</span><span class="sxs-lookup"><span data-stu-id="1d93a-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-144">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1d93a-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-145">**17**</span><span class="sxs-lookup"><span data-stu-id="1d93a-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-146">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="1d93a-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1d93a-147">**21**</span><span class="sxs-lookup"><span data-stu-id="1d93a-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1d93a-148">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1d93a-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d93a-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d93a-149">Requirements</span></span>



| <span data-ttu-id="1d93a-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d93a-150">Requirement</span></span> | <span data-ttu-id="1d93a-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d93a-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d93a-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d93a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1d93a-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d93a-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d93a-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d93a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1d93a-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d93a-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d93a-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d93a-156">Namespace</span></span><br/>                | <span data-ttu-id="1d93a-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d93a-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d93a-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1d93a-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d93a-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d93a-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d93a-160">DLL</span><span class="sxs-lookup"><span data-stu-id="1d93a-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d93a-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d93a-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d93a-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d93a-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d93a-163">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d93a-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d93a-164">**\_CodecFile Win32**</span><span class="sxs-lookup"><span data-stu-id="1d93a-164">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

