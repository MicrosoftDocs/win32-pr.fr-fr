---
description: La méthode Delete WMI Class supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513331"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="6a7f9-103">Méthode Delete de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="6a7f9-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="6a7f9-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime le fichier logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="6a7f9-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a7f9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a7f9-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a7f9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7f9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a7f9-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="6a7f9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a7f9-108">Parameters</span></span>

<span data-ttu-id="6a7f9-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a7f9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a7f9-110">Return value</span></span>

<span data-ttu-id="6a7f9-111">Retourne la valeur 0 (zéro) si le fichier a été supprimé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a7f9-112">**0**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-114">**2**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-116">**8**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-118">**9**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-120">**10**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-122">**11**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-124">**12**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-126">**13**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-128">**14**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-130">**15**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-132">**16**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-134">**17**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6a7f9-136">**21**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6a7f9-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a7f9-138">Notes</span><span class="sxs-lookup"><span data-stu-id="6a7f9-138">Remarks</span></span>

<span data-ttu-id="6a7f9-139">Les dossiers ne sont pas nécessairement des ajouts permanents à un système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="6a7f9-140">À un moment donné, vous devrez peut-être supprimer des dossiers, peut-être parce qu’ils ne sont plus nécessaires, car le rôle de l’ordinateur a changé ou parce que les dossiers ont été créés par erreur.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="6a7f9-141">Supprimer vous permet de supprimer des dossiers : il vous suffit de lier au dossier en question, puis d’appeler la méthode Delete.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="6a7f9-142">Une fois la méthode Delete appelée, le dossier est supprimé définitivement du système de fichiers ; elle n’est pas envoyée à la corbeille.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="6a7f9-143">En outre, aucun avis de confirmation (« êtes-vous sûr de vouloir supprimer ce dossier ? ») est émis.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="6a7f9-144">Au lieu de cela, le dossier est immédiatement supprimé.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="6a7f9-145">Vous ne pouvez pas supprimer des dossiers en lecture seule à l’aide de FileSystemObject ; Toutefois, cette opération peut être effectuée à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="6a7f9-146">Si votre script utilise WMI et que vous ne souhaitez pas supprimer un dossier en lecture seule, vous devez utiliser la propriété lisible pour vérifier l’état du dossier avant de le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="6a7f9-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="6a7f9-147">Examples</span></span>

<span data-ttu-id="6a7f9-148">L’exemple de code VBScript suivant supprime le dossier C : \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="6a7f9-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a7f9-149">Requirements</span></span>



| <span data-ttu-id="6a7f9-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a7f9-150">Requirement</span></span> | <span data-ttu-id="6a7f9-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a7f9-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7f9-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a7f9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6a7f9-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a7f9-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a7f9-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a7f9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6a7f9-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a7f9-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a7f9-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a7f9-156">Namespace</span></span><br/>                | <span data-ttu-id="6a7f9-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6a7f9-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a7f9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="6a7f9-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a7f9-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a7f9-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a7f9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="6a7f9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a7f9-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a7f9-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7f9-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a7f9-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a7f9-163">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a7f9-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a7f9-164">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="6a7f9-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

