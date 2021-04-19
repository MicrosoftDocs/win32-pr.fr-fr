---
description: Obtient la propriété du fichier de raccourci logique spécifié dans le chemin d’accès de l’objet. Cette méthode est une version étendue de la méthode TakeOwnerShip.
ms.assetid: 1345562c-343e-4e3a-b6ed-3b64a7260c89
ms.tgt_platform: multiple
title: Méthode TakeOwnerShipEx de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69988c7995ee295297c92bbabf0ee83059304a94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516363"
---
# <a name="takeownershipex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="1231b-104">Méthode TakeOwnerShipEx de la \_ classe Win32 ShortcutFile</span><span class="sxs-lookup"><span data-stu-id="1231b-104">TakeOwnerShipEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="1231b-105">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtient la propriété du fichier de raccourci logique spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1231b-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="1231b-106">Cette méthode est une version étendue de la méthode [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="1231b-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="1231b-107">Si le fichier logique est effectivement un répertoire, cette méthode agit de manière récursive, en prenant possession de tous les fichiers et sous-répertoires contenus dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="1231b-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="1231b-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1231b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1231b-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1231b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1231b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1231b-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1231b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1231b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1231b-112">*StopFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1231b-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1231b-113">Nom du fichier ou du répertoire dans lequel la méthode **TakeOwnerShipEx** a échoué.</span><span class="sxs-lookup"><span data-stu-id="1231b-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="1231b-114">Ce paramètre a la **valeur null** si la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="1231b-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-115">*StartFileName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1231b-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1231b-116">Nomme le fichier ou le répertoire enfant à utiliser comme point de départ pour **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="1231b-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="1231b-117">Le paramètre *StartFileName* est généralement le paramètre *StopFileName* spécifiant le fichier ou le répertoire dans lequel une erreur s’est produite à partir de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="1231b-117">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1231b-118">Si ce paramètre a la **valeur null**, l’opération est effectuée sur le fichier ou le répertoire spécifié dans l’appel de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="1231b-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-119">*Récursif* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1231b-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1231b-120">Si la **valeur est true**, la modification de la propriété sera appliquée de manière récursive aux fichiers et aux répertoires dans le répertoire spécifié par l’instance [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1231b-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="1231b-121">Pour les instances de fichier, le paramètre *recursive* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1231b-121">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1231b-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1231b-122">Return value</span></span>

<span data-ttu-id="1231b-123">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1231b-123">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1231b-124">**0**</span><span class="sxs-lookup"><span data-stu-id="1231b-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-125">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="1231b-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-126">**2**</span><span class="sxs-lookup"><span data-stu-id="1231b-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-127">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="1231b-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-128">**8**</span><span class="sxs-lookup"><span data-stu-id="1231b-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-129">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1231b-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-130">**9**</span><span class="sxs-lookup"><span data-stu-id="1231b-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-131">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1231b-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-132">**10**</span><span class="sxs-lookup"><span data-stu-id="1231b-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-133">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="1231b-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-134">**11**</span><span class="sxs-lookup"><span data-stu-id="1231b-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-135">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="1231b-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-136">**12**</span><span class="sxs-lookup"><span data-stu-id="1231b-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-137">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="1231b-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-138">**13**</span><span class="sxs-lookup"><span data-stu-id="1231b-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-139">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="1231b-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-140">**14**</span><span class="sxs-lookup"><span data-stu-id="1231b-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-141">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="1231b-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-142">**15**</span><span class="sxs-lookup"><span data-stu-id="1231b-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-143">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1231b-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-144">**16**</span><span class="sxs-lookup"><span data-stu-id="1231b-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-145">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1231b-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-146">**17**</span><span class="sxs-lookup"><span data-stu-id="1231b-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-147">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="1231b-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1231b-148">**21**</span><span class="sxs-lookup"><span data-stu-id="1231b-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1231b-149">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1231b-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1231b-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1231b-150">Requirements</span></span>



| <span data-ttu-id="1231b-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1231b-151">Requirement</span></span> | <span data-ttu-id="1231b-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="1231b-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1231b-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1231b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1231b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1231b-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1231b-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1231b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1231b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1231b-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1231b-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1231b-157">Namespace</span></span><br/>                | <span data-ttu-id="1231b-158">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1231b-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1231b-159">MOF</span><span class="sxs-lookup"><span data-stu-id="1231b-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1231b-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1231b-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1231b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="1231b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1231b-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1231b-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1231b-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1231b-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="1231b-164">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1231b-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1231b-165">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="1231b-165">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

