---
description: La fonction UiCreatePatchPackageEx prend un fichier de création de package (fichier. PCP) et génère une Windows Installer package correctif (package. msp). L’appel de Msimsp.exe est la méthode recommandée pour utiliser Patchwiz.dll.
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: UiCreatePatchPackageEx (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac61371d1e7bf1809880c8f10a403d1730adc8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516818"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a><span data-ttu-id="78b54-104">UiCreatePatchPackageEx (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="78b54-104">UiCreatePatchPackageEx (Patchwiz.dll)</span></span>

<span data-ttu-id="78b54-105">La fonction UiCreatePatchPackageEx prend un fichier de création de package (fichier. PCP) et génère une Windows Installer package correctif (package. msp).</span><span class="sxs-lookup"><span data-stu-id="78b54-105">The UiCreatePatchPackageEx function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="78b54-106">L’appel de [Msimsp.exe](msimsp-exe.md) est la méthode recommandée pour utiliser [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="78b54-106">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span>

<span data-ttu-id="78b54-107">La fonction UiCreatePatchPackageEx est disponible à partir de Patchwiz.dll version 4,0 et étend les fonctionnalités de la fonction [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="78b54-107">The UiCreatePatchPackageEx function is available beginning with Patchwiz.dll version 4.0 and extends the functionality of the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a><span data-ttu-id="78b54-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78b54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78b54-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="78b54-109"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-110">Chemin d’accès complet au fichier de propriétés de création de correctif (fichier. PCP) de ce correctif.</span><span class="sxs-lookup"><span data-stu-id="78b54-110">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="78b54-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="78b54-111"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-112">Chemin d’accès complet au package de correctifs Windows Installer (fichier. msp) à créer.</span><span class="sxs-lookup"><span data-stu-id="78b54-112">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="78b54-113">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="78b54-113">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="78b54-114">Si la valeur est **null** ou est une chaîne vide, la fonction utilise la valeur de PatchOutputPath dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="78b54-114">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="78b54-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="78b54-115"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-116">Chemin d’accès complet à un fichier journal texte qui sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="78b54-116">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="78b54-117">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="78b54-117">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="78b54-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="78b54-118"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-119">Handle d’une fenêtre qui affiche le texte d’État.</span><span class="sxs-lookup"><span data-stu-id="78b54-119">Handle to a window that displays the status text.</span></span> <span data-ttu-id="78b54-120">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="78b54-120">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="78b54-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="78b54-121"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-122">Emplacement des fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="78b54-122">Location for temporary files.</span></span> <span data-ttu-id="78b54-123">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="78b54-123">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="78b54-124">L’utilisateur doit disposer des privilèges suffisants pour lire et écrire dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="78b54-124">The user must have sufficient privileges to read and write to this folder.</span></span> <span data-ttu-id="78b54-125">L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="78b54-125">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="78b54-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="78b54-126"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-127">Si la **valeur est true**, supprimez le dossier temporaire et tout son contenu, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="78b54-127">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="78b54-128">Si la **valeur est false** et que le dossier est présent, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="78b54-128">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="78b54-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="78b54-129"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-130">Ce paramètre peut prendre la valeur d’une ou d’une combinaison des valeurs suivantes pour spécifier les options de journalisation ou d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78b54-130">This parameter can be set to one or a combination of the following values to specify logging or user interface options.</span></span>



| <span data-ttu-id="78b54-131">Indicateur</span><span class="sxs-lookup"><span data-stu-id="78b54-131">Flag</span></span>            | <span data-ttu-id="78b54-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="78b54-132">Value</span></span>       | <span data-ttu-id="78b54-133">Signification</span><span class="sxs-lookup"><span data-stu-id="78b54-133">Meaning</span></span>                                  |
|-----------------|-------------|------------------------------------------|
| <span data-ttu-id="78b54-134">LOGNONE</span><span class="sxs-lookup"><span data-stu-id="78b54-134">LOGNONE</span></span>         | <span data-ttu-id="78b54-135">0x00000000</span><span class="sxs-lookup"><span data-stu-id="78b54-135">0x00000000</span></span>  | <span data-ttu-id="78b54-136">Écrire aucun message dans le journal.</span><span class="sxs-lookup"><span data-stu-id="78b54-136">Write no messages to the log.</span></span>            |
| <span data-ttu-id="78b54-137">LOGINFO</span><span class="sxs-lookup"><span data-stu-id="78b54-137">LOGINFO</span></span>         | <span data-ttu-id="78b54-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="78b54-138">0x00000001</span></span>  | <span data-ttu-id="78b54-139">Écrire des messages d’information dans le journal.</span><span class="sxs-lookup"><span data-stu-id="78b54-139">Write informational messages to the log.</span></span> |
| <span data-ttu-id="78b54-140">LOGWARN</span><span class="sxs-lookup"><span data-stu-id="78b54-140">LOGWARN</span></span>         | <span data-ttu-id="78b54-141">0x00000002</span><span class="sxs-lookup"><span data-stu-id="78b54-141">0x00000002</span></span>  | <span data-ttu-id="78b54-142">Écrire les avertissements dans le journal.</span><span class="sxs-lookup"><span data-stu-id="78b54-142">Write warnings to the log.</span></span>               |
| <span data-ttu-id="78b54-143">LOGERR</span><span class="sxs-lookup"><span data-stu-id="78b54-143">LOGERR</span></span>          | <span data-ttu-id="78b54-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="78b54-144">0x00000004</span></span>  | <span data-ttu-id="78b54-145">Écrire les messages d’erreur dans le journal.</span><span class="sxs-lookup"><span data-stu-id="78b54-145">Write error messages to the log.</span></span>         |
| <span data-ttu-id="78b54-146">LOGPERFMESSAGES</span><span class="sxs-lookup"><span data-stu-id="78b54-146">LOGPERFMESSAGES</span></span> | <span data-ttu-id="78b54-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="78b54-147">0x00000008</span></span>  | <span data-ttu-id="78b54-148">Écrire les messages de performance dans le journal.</span><span class="sxs-lookup"><span data-stu-id="78b54-148">Write performance messages to the log.</span></span>   |
| <span data-ttu-id="78b54-149">UINONE</span><span class="sxs-lookup"><span data-stu-id="78b54-149">UINONE</span></span>          | <span data-ttu-id="78b54-150">0x00000000f</span><span class="sxs-lookup"><span data-stu-id="78b54-150">0x00000000f</span></span> | <span data-ttu-id="78b54-151">N’affiche pas l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78b54-151">Do not display the user interface.</span></span>       |
| <span data-ttu-id="78b54-152">UIALL</span><span class="sxs-lookup"><span data-stu-id="78b54-152">UIALL</span></span>           | <span data-ttu-id="78b54-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="78b54-153">0x00000010</span></span>  | <span data-ttu-id="78b54-154">Affichez l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78b54-154">Display the user interface.</span></span>              |



 

</dd> <dt>

<span data-ttu-id="78b54-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="78b54-155"><span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*</span></span>
</dt> <dd>

<span data-ttu-id="78b54-156">Réservé.</span><span class="sxs-lookup"><span data-stu-id="78b54-156">Reserved.</span></span> <span data-ttu-id="78b54-157">Ce paramètre doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="78b54-157">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="78b54-158">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="78b54-158">Return Values</span></span>

<span data-ttu-id="78b54-159">Consultez le tableau dans [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="78b54-159">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78b54-160">Notes</span><span class="sxs-lookup"><span data-stu-id="78b54-160">Remarks</span></span>

<span data-ttu-id="78b54-161">Pour obtenir un exemple de création d’un fichier. PCP et l’utilisation de [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) pour générer un package de correctifs Windows Installer, consultez la section [exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="78b54-161">For an example of authoring a .pcp file and using [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="78b54-162">La création d’un correctif requiert une image d’installation non compressée, telle qu’une image administrative ou une image d’installation non compressée à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="78b54-162">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="78b54-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) ne génère pas de correctifs binaires pour les fichiers dans les armoires.</span><span class="sxs-lookup"><span data-stu-id="78b54-163">[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) does not generate binary patches for files in cabinets.</span></span>

 

 



