---
description: Obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519203"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="d493a-104">Méthode TakeOwnerShipEx de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="d493a-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="d493a-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtient la propriété du fichier d’entrée de répertoire logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d493a-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="d493a-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="d493a-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="d493a-107">Si le fichier logique est effectivement un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="d493a-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="d493a-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d493a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d493a-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d493a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d493a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d493a-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="d493a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d493a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d493a-112">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d493a-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d493a-113">Nom du fichier ou du répertoire dans lequel la méthode **TakeOwnerShipEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="d493a-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="d493a-114">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="d493a-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-115">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d493a-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d493a-116">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="d493a-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="d493a-117">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* qui spécifie le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="d493a-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d493a-118">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="d493a-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="d493a-119">Si *il* est utilisé, la valeur *recursive* doit également être définie sur true.</span><span class="sxs-lookup"><span data-stu-id="d493a-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-120">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d493a-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d493a-121">Si la **valeur est true**, la modification de la propriété est appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d493a-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="d493a-122">Pour les instances de fichier, le paramètre d’entrée *récursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="d493a-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d493a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d493a-123">Return value</span></span>

<span data-ttu-id="d493a-124">Retourne une valeur entière égale à 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d493a-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d493a-125">**0**</span><span class="sxs-lookup"><span data-stu-id="d493a-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-126">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="d493a-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-127">**2**</span><span class="sxs-lookup"><span data-stu-id="d493a-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-128">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="d493a-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-129">**8**</span><span class="sxs-lookup"><span data-stu-id="d493a-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-130">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d493a-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-131">**9**</span><span class="sxs-lookup"><span data-stu-id="d493a-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-132">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d493a-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-133">**10**</span><span class="sxs-lookup"><span data-stu-id="d493a-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-134">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d493a-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-135">**11**</span><span class="sxs-lookup"><span data-stu-id="d493a-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-136">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="d493a-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-137">**12**</span><span class="sxs-lookup"><span data-stu-id="d493a-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-138">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="d493a-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-139">**13**</span><span class="sxs-lookup"><span data-stu-id="d493a-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-140">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="d493a-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-141">**14**</span><span class="sxs-lookup"><span data-stu-id="d493a-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-142">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="d493a-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-143">**15**</span><span class="sxs-lookup"><span data-stu-id="d493a-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-144">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d493a-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-145">**16**</span><span class="sxs-lookup"><span data-stu-id="d493a-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-146">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d493a-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-147">**17**</span><span class="sxs-lookup"><span data-stu-id="d493a-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-148">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="d493a-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d493a-149">**21**</span><span class="sxs-lookup"><span data-stu-id="d493a-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d493a-150">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d493a-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d493a-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="d493a-151">Examples</span></span>

<span data-ttu-id="d493a-152">L’Visual Basic Code de script suivant appelle la méthode [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) pour prendre possession du dossier C : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="d493a-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="d493a-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d493a-153">Requirements</span></span>



| <span data-ttu-id="d493a-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d493a-154">Requirement</span></span> | <span data-ttu-id="d493a-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="d493a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d493a-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d493a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d493a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d493a-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d493a-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d493a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d493a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d493a-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d493a-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d493a-160">Namespace</span></span><br/>                | <span data-ttu-id="d493a-161">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d493a-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d493a-162">MOF</span><span class="sxs-lookup"><span data-stu-id="d493a-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d493a-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d493a-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d493a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="d493a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d493a-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d493a-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d493a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d493a-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="d493a-167">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d493a-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d493a-168">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="d493a-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

