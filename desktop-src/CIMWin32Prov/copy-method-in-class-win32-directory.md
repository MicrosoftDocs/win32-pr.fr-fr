---
description: Copie le fichier d’entrée de répertoire logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Méthode Copy de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110807"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="94bc4-103">Méthode Copy de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="94bc4-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="94bc4-104">La méthode **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copie le fichier d’entrée de répertoire logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="94bc4-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="94bc4-105">Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="94bc4-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="94bc4-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="94bc4-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94bc4-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94bc4-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94bc4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94bc4-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="94bc4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94bc4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94bc4-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="94bc4-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="94bc4-111">Nom complet de la copie du fichier (ou du répertoire).</span><span class="sxs-lookup"><span data-stu-id="94bc4-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="94bc4-112">Exemple : c : \\ temp \\ newDirectory</span><span class="sxs-lookup"><span data-stu-id="94bc4-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94bc4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94bc4-113">Return value</span></span>

<span data-ttu-id="94bc4-114">Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="94bc4-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="94bc4-115">**0**</span><span class="sxs-lookup"><span data-stu-id="94bc4-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-116">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="94bc4-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-117">**2**</span><span class="sxs-lookup"><span data-stu-id="94bc4-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-118">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="94bc4-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-119">**8**</span><span class="sxs-lookup"><span data-stu-id="94bc4-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-120">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="94bc4-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-121">**9**</span><span class="sxs-lookup"><span data-stu-id="94bc4-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-122">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="94bc4-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-123">**10**</span><span class="sxs-lookup"><span data-stu-id="94bc4-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-124">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="94bc4-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-125">**11**</span><span class="sxs-lookup"><span data-stu-id="94bc4-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-126">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="94bc4-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-127">**12**</span><span class="sxs-lookup"><span data-stu-id="94bc4-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-128">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="94bc4-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-129">**13**</span><span class="sxs-lookup"><span data-stu-id="94bc4-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-130">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="94bc4-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-131">**14**</span><span class="sxs-lookup"><span data-stu-id="94bc4-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-132">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="94bc4-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-133">**15**</span><span class="sxs-lookup"><span data-stu-id="94bc4-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-134">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="94bc4-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-135">**16**</span><span class="sxs-lookup"><span data-stu-id="94bc4-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-136">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="94bc4-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-137">**17**</span><span class="sxs-lookup"><span data-stu-id="94bc4-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-138">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="94bc4-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="94bc4-139">**21**</span><span class="sxs-lookup"><span data-stu-id="94bc4-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="94bc4-140">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="94bc4-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94bc4-141">Notes</span><span class="sxs-lookup"><span data-stu-id="94bc4-141">Remarks</span></span>

<span data-ttu-id="94bc4-142">Les dossiers doivent souvent être copiés d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="94bc4-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="94bc4-143">Par exemple, vous pouvez copier un dossier d’un serveur vers un autre pour créer une copie de sauvegarde de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="94bc4-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="94bc4-144">Vous pouvez également avoir un dossier de modèles qui doit être copié sur les stations de travail des utilisateurs ou un dossier de scripts qui doit être copié sur tous vos serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="94bc4-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="94bc4-145">La \_ méthode de copie d’annuaire Win32 vous permet de copier un dossier d’un emplacement à un autre, sur le même ordinateur (par exemple, en copiant un dossier du lecteur C vers le lecteur D) ou sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="94bc4-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="94bc4-146">Pour copier un dossier, vous devez retourner une instance du dossier à copier, puis appeler la méthode Copy, en passant en tant que paramètre l’emplacement cible de la nouvelle copie du dossier.</span><span class="sxs-lookup"><span data-stu-id="94bc4-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="94bc4-147">Par exemple, cette ligne de code copie un dossier dans le dossier scripts sur le lecteur F :</span><span class="sxs-lookup"><span data-stu-id="94bc4-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="94bc4-148">WMI ne remplacera pas un dossier existant lors de l’exécution de la méthode de copie.</span><span class="sxs-lookup"><span data-stu-id="94bc4-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="94bc4-149">Cela signifie que l’opération de copie échoue si le dossier de destination existe.</span><span class="sxs-lookup"><span data-stu-id="94bc4-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="94bc4-150">Supposons, par exemple, que vous avez un dossier nommé scripts et que vous tentez de copier ce dossier sur un partage distant nommé \\ \\ Archive ATL-FS-01 \\ .</span><span class="sxs-lookup"><span data-stu-id="94bc4-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="94bc4-151">Si un dossier nommé scripts existe déjà sur ce partage, l’opération de copie échoue.</span><span class="sxs-lookup"><span data-stu-id="94bc4-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="94bc4-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="94bc4-152">Examples</span></span>

<span data-ttu-id="94bc4-153">L’exemple de code proposition, extrait de la [copie d’un dossier à l’aide de WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), utilise la méthode Copy pour copier le dossier C : \\ scripts vers D : \\ archive.</span><span class="sxs-lookup"><span data-stu-id="94bc4-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="94bc4-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94bc4-154">Requirements</span></span>



| <span data-ttu-id="94bc4-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94bc4-155">Requirement</span></span> | <span data-ttu-id="94bc4-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="94bc4-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94bc4-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94bc4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="94bc4-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94bc4-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94bc4-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94bc4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="94bc4-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94bc4-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94bc4-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94bc4-161">Namespace</span></span><br/>                | <span data-ttu-id="94bc4-162">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="94bc4-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94bc4-163">MOF</span><span class="sxs-lookup"><span data-stu-id="94bc4-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94bc4-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94bc4-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94bc4-165">DLL</span><span class="sxs-lookup"><span data-stu-id="94bc4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94bc4-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94bc4-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94bc4-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94bc4-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="94bc4-168">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94bc4-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="94bc4-169">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="94bc4-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

