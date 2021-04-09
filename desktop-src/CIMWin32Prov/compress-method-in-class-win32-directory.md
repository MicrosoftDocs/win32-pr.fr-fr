---
description: Compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Méthode Compress de la classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110246"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="35f5d-103">Méthode Compress de la \_ classe Directory Win32</span><span class="sxs-lookup"><span data-stu-id="35f5d-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="35f5d-104">La méthode de classe **compresser** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) compresse le fichier d’entrée de répertoire logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35f5d-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="35f5d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="35f5d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="35f5d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="35f5d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="35f5d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35f5d-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="35f5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35f5d-108">Parameters</span></span>

<span data-ttu-id="35f5d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="35f5d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35f5d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35f5d-110">Return value</span></span>

<span data-ttu-id="35f5d-111">Retourne la valeur 0 (zéro) si le fichier a été compressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="35f5d-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="35f5d-112">**0**</span><span class="sxs-lookup"><span data-stu-id="35f5d-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="35f5d-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-114">**2**</span><span class="sxs-lookup"><span data-stu-id="35f5d-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="35f5d-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-116">**8**</span><span class="sxs-lookup"><span data-stu-id="35f5d-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="35f5d-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-118">**9**</span><span class="sxs-lookup"><span data-stu-id="35f5d-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35f5d-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-120">**10**</span><span class="sxs-lookup"><span data-stu-id="35f5d-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="35f5d-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-122">**11**</span><span class="sxs-lookup"><span data-stu-id="35f5d-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="35f5d-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-124">**12**</span><span class="sxs-lookup"><span data-stu-id="35f5d-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="35f5d-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-126">**13**</span><span class="sxs-lookup"><span data-stu-id="35f5d-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="35f5d-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-128">**14**</span><span class="sxs-lookup"><span data-stu-id="35f5d-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="35f5d-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-130">**15**</span><span class="sxs-lookup"><span data-stu-id="35f5d-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="35f5d-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-132">**16**</span><span class="sxs-lookup"><span data-stu-id="35f5d-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35f5d-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-134">**17**</span><span class="sxs-lookup"><span data-stu-id="35f5d-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="35f5d-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="35f5d-136">**21**</span><span class="sxs-lookup"><span data-stu-id="35f5d-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="35f5d-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35f5d-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35f5d-138">Notes</span><span class="sxs-lookup"><span data-stu-id="35f5d-138">Remarks</span></span>

<span data-ttu-id="35f5d-139">La compression permet de libérer de l’espace de stockage supplémentaire sur un lecteur de disque sans acheter de nouveau matériel ni supprimer de fichiers ou de dossiers.</span><span class="sxs-lookup"><span data-stu-id="35f5d-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="35f5d-140">En fonction de la taille de votre disque dur et du type de fichiers stockés sur ce disque, vous pouvez récupérer des centaines de mégaoctets d’espace disque et, par conséquent, éviter d’acheter un nouveau disque dur et de mettre l’ordinateur hors connexion jusqu’à ce que le nouveau lecteur soit installé.</span><span class="sxs-lookup"><span data-stu-id="35f5d-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="35f5d-141">La méthode Compress compresse tous les fichiers et sous-dossiers dans un dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="35f5d-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="35f5d-142">En outre, la classe comprend également une méthode decompress qui supprime la compression de tous les fichiers et sous-dossiers d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="35f5d-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="35f5d-143">Des méthodes similaires sont également fournies avec la \_ classe de fichier de fichier CIM.</span><span class="sxs-lookup"><span data-stu-id="35f5d-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="35f5d-144">Cela vous permet de compresser ou de décompresser de manière sélective des fichiers spécifiques dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="35f5d-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="35f5d-145">Dans la mesure où la compression réduit légèrement les performances, il n’est pas recommandé pour les fichiers ou dossiers accessibles sur une base régulière. par exemple, vous ne souhaitez probablement pas compresser des fichiers de base de données, des fichiers journaux ou des dossiers de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35f5d-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="35f5d-146">Les meilleurs candidats à la compression sont les fichiers et les dossiers qui ne sont pas très souvent utilisés.</span><span class="sxs-lookup"><span data-stu-id="35f5d-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="35f5d-147">Par exemple, vous pouvez écrire un script pour retourner une collection de dossiers sur un lecteur qui n’a pas été consulté depuis un mois ou plus, puis compresser chacun de ces dossiers.</span><span class="sxs-lookup"><span data-stu-id="35f5d-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="35f5d-148">La quantité d’espace disque libérée par la compression des dossiers varie selon le type de fichier stocké dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="35f5d-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="35f5d-149">Par exemple, les fichiers. jpg sont déjà compressés et la compression n’a que peu d’effet sur la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="35f5d-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="35f5d-150">Toutefois, avec d’autres types de fichiers, les économies peuvent être considérables.</span><span class="sxs-lookup"><span data-stu-id="35f5d-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="35f5d-151">Par exemple, un nouveau dossier a été créé sur un ordinateur de test Windows 2000 et 33 documents Microsoft Word, qui occupent un total de 15 mégaoctets (Mo) d’espace disque, ont été copiés dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="35f5d-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="35f5d-152">Lorsque les documents ont été compressés, le dossier n’a pris que 7 Mo d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="35f5d-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="35f5d-153">Exemples</span><span class="sxs-lookup"><span data-stu-id="35f5d-153">Examples</span></span>

<span data-ttu-id="35f5d-154">L’exemple VBScript suivant compresse le dossier C : \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="35f5d-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="35f5d-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35f5d-155">Requirements</span></span>



| <span data-ttu-id="35f5d-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35f5d-156">Requirement</span></span> | <span data-ttu-id="35f5d-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="35f5d-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f5d-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35f5d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="35f5d-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35f5d-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35f5d-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35f5d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="35f5d-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35f5d-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35f5d-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35f5d-162">Namespace</span></span><br/>                | <span data-ttu-id="35f5d-163">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="35f5d-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35f5d-164">MOF</span><span class="sxs-lookup"><span data-stu-id="35f5d-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35f5d-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35f5d-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35f5d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="35f5d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f5d-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f5d-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f5d-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35f5d-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="35f5d-169">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35f5d-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="35f5d-170">**\_Répertoire Win32**</span><span class="sxs-lookup"><span data-stu-id="35f5d-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="35f5d-171">**Décompresser**</span><span class="sxs-lookup"><span data-stu-id="35f5d-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

