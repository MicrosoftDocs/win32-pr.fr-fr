---
description: Renomme le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517170"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="3bb4e-103">Renommer la méthode de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="3bb4e-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="3bb4e-104">La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="3bb4e-105">Un changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="3bb4e-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3bb4e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3bb4e-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3bb4e-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb4e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bb4e-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3bb4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bb4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb4e-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="3bb4e-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb4e-111">Nouveau nom complet du fichier (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="3bb4e-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="3bb4e-112">Exemple : c : \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb4e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bb4e-113">Return value</span></span>

<span data-ttu-id="3bb4e-114">Retourne la valeur 0 (zéro) si le fichier a été renommé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3bb4e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-116">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-117">**2**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-118">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-119">**8**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-120">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-121">**9**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-122">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-123">**10**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-124">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-125">**11**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-126">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-127">**12**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-128">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-129">**13**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-130">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-131">**14**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-132">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-133">**15**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-134">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-135">**16**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-136">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-137">**17**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-138">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3bb4e-139">**21**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3bb4e-140">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bb4e-141">Notes</span><span class="sxs-lookup"><span data-stu-id="3bb4e-141">Remarks</span></span>

<span data-ttu-id="3bb4e-142">Pour renommer un dossier, commencez par lier le dossier en question, puis appelez la méthode Rename.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="3bb4e-143">Comme seul paramètre de la méthode, transmettez le nouveau nom du dossier sous la forme d’un nom de chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="3bb4e-144">Par exemple, si le dossier de la \\ sauvegarde journaux c : scripts doit \\ \\ être renommé en c : \\ scripts \\ Archive, vous devez passer l’archive c : \\ scripts \\ comme nom de dossier complet.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="3bb4e-145">Le passage uniquement du nom de dossier-archive-génère une erreur de chemin d’accès non valide.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="3bb4e-146">La \_ classe de répertoire Win32 ne fournit pas de méthode en une étape pour déplacer des dossiers.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="3bb4e-147">Au lieu de cela, le déplacement d’un dossier implique généralement deux étapes :</span><span class="sxs-lookup"><span data-stu-id="3bb4e-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="3bb4e-148">Copie du dossier vers son nouvel emplacement</span><span class="sxs-lookup"><span data-stu-id="3bb4e-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="3bb4e-149">Suppression du dossier d’origine</span><span class="sxs-lookup"><span data-stu-id="3bb4e-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="3bb4e-150">La seule exception à ce processus en deux étapes implique le déplacement d’un dossier vers un nouvel emplacement sur le même lecteur.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="3bb4e-151">Supposons, par exemple, que vous souhaitiez déplacer l' \\ Archive de fichiers temporaires c : Temp vers c : \\ scripts \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="3bb4e-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="3bb4e-152">Tant que l’emplacement actuel et le nouvel emplacement se trouvent sur le même lecteur, vous pouvez déplacer le dossier en appelant simplement la méthode Rename et en passant le nouvel emplacement en tant que paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="3bb4e-153">Cette approche vous permet de déplacer le dossier en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="3bb4e-154">Toutefois, le script échoue si le lecteur actif et le nouveau lecteur sont différents.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="3bb4e-155">Une tentative de changement de nom de C : \\ temp en D : \\ temp échoue avec une erreur « lecteur non identique ».</span><span class="sxs-lookup"><span data-stu-id="3bb4e-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="3bb4e-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="3bb4e-156">Examples</span></span>

<span data-ttu-id="3bb4e-157">Le code suivant, extrait de l’exemple de [déplacement d’un dossier à l’aide](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) de VBScript WMI sur la Galerie TechNet, utilise la méthode Rename pour déplacer le dossier c : \\ scripts vers c : \\ admins \\ documents \\ Archive \\ VBScript.</span><span class="sxs-lookup"><span data-stu-id="3bb4e-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="3bb4e-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bb4e-158">Requirements</span></span>



| <span data-ttu-id="3bb4e-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bb4e-159">Requirement</span></span> | <span data-ttu-id="3bb4e-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bb4e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb4e-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bb4e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb4e-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bb4e-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bb4e-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bb4e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb4e-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bb4e-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bb4e-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3bb4e-165">Namespace</span></span><br/>                | <span data-ttu-id="3bb4e-166">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3bb4e-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3bb4e-167">MOF</span><span class="sxs-lookup"><span data-stu-id="3bb4e-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bb4e-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bb4e-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bb4e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb4e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb4e-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bb4e-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb4e-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bb4e-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bb4e-172">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3bb4e-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3bb4e-173">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="3bb4e-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

