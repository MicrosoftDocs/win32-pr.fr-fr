---
description: La fonction UiCreatePatchPackage prend un fichier de création de package (fichier. PCP) et génère une Windows Installer package correctif (package. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861901"
---
# <a name="uicreatepatchpackage-patchwizdll"></a><span data-ttu-id="8fd82-103">UiCreatePatchPackage (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="8fd82-103">UiCreatePatchPackage (Patchwiz.dll)</span></span>

<span data-ttu-id="8fd82-104">La fonction UiCreatePatchPackage prend un fichier de création de package (fichier. PCP) et génère une Windows Installer package correctif (package. msp).</span><span class="sxs-lookup"><span data-stu-id="8fd82-104">The UiCreatePatchPackage function takes a package creation file (.pcp file) and generates a Windows Installer patch package (.msp package).</span></span> <span data-ttu-id="8fd82-105">L’appel de [Msimsp.exe](msimsp-exe.md) est la méthode recommandée pour utiliser [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="8fd82-105">Calling [Msimsp.exe](msimsp-exe.md) is the recommended method for using [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="8fd82-106">La fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) est disponible dans la version 4,0 de Patchwiz.dll et étend les fonctionnalités de la fonction UiCreatePatchPackage.</span><span class="sxs-lookup"><span data-stu-id="8fd82-106">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function is available in version 4.0 of Patchwiz.dll and extends the functionality of the UiCreatePatchPackage function.</span></span>

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
);
```

## <a name="parameters"></a><span data-ttu-id="8fd82-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fd82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd82-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span><span class="sxs-lookup"><span data-stu-id="8fd82-108"><span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-109">Chemin d’accès complet au fichier de propriétés de création de correctif (fichier. PCP) de ce correctif.</span><span class="sxs-lookup"><span data-stu-id="8fd82-109">Full path to the patch creation properties file (.pcp file) for this patch.</span></span>

</dd> <dt>

<span data-ttu-id="8fd82-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span><span class="sxs-lookup"><span data-stu-id="8fd82-110"><span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-111">Chemin d’accès complet au package de correctifs Windows Installer (fichier. msp) à créer.</span><span class="sxs-lookup"><span data-stu-id="8fd82-111">Full path to the Windows Installer patch package (.msp file) that is to be created.</span></span> <span data-ttu-id="8fd82-112">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="8fd82-112">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="8fd82-113">Si la valeur est **null** ou est une chaîne vide, la fonction utilise la valeur de PatchOutputPath dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="8fd82-113">If it is **NULL** or an empty string, the function uses the value of PatchOutputPath in the [Properties Table (Patchwiz.dll)](properties-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd82-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="8fd82-114"><span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-115">Chemin d’accès complet à un fichier journal texte qui sera ajouté.</span><span class="sxs-lookup"><span data-stu-id="8fd82-115">Full path to a text log file that will be appended.</span></span> <span data-ttu-id="8fd82-116">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="8fd82-116">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="8fd82-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span><span class="sxs-lookup"><span data-stu-id="8fd82-117"><span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-118">Handle d’une fenêtre qui affiche le texte d’État.</span><span class="sxs-lookup"><span data-stu-id="8fd82-118">Handle to a window that displays the status text.</span></span> <span data-ttu-id="8fd82-119">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="8fd82-119">This parameter may be **NULL** or an empty string but may not be omitted.</span></span>

</dd> <dt>

<span data-ttu-id="8fd82-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span><span class="sxs-lookup"><span data-stu-id="8fd82-120"><span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-121">Emplacement des fichiers temporaires.</span><span class="sxs-lookup"><span data-stu-id="8fd82-121">Location for temporary files.</span></span> <span data-ttu-id="8fd82-122">Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.</span><span class="sxs-lookup"><span data-stu-id="8fd82-122">This parameter may be **NULL** or an empty string but may not be omitted.</span></span> <span data-ttu-id="8fd82-123">L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="8fd82-123">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="8fd82-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span><span class="sxs-lookup"><span data-stu-id="8fd82-124"><span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*</span></span>
</dt> <dd>

<span data-ttu-id="8fd82-125">Si la **valeur est true**, supprimez le dossier temporaire et tout son contenu, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8fd82-125">If **TRUE**, remove the temporary folder and all of its contents if present.</span></span> <span data-ttu-id="8fd82-126">Si la **valeur est false** et que le dossier est présent, la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="8fd82-126">If **FALSE**, and folder is present, the function fails.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="8fd82-127">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8fd82-127">Return Values</span></span>

<span data-ttu-id="8fd82-128">Consultez le tableau dans [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8fd82-128">See the table in [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fd82-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8fd82-129">Remarks</span></span>

<span data-ttu-id="8fd82-130">Pour obtenir un exemple de création d’un fichier. PCP et l’utilisation de UiCreatePatchPackage pour générer un package de correctifs Windows Installer, consultez la section [exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="8fd82-130">For an example of authoring a .pcp file and using UiCreatePatchPackage to generate a Windows Installer patch package, see the section [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="8fd82-131">La création d’un correctif requiert une image d’installation non compressée, telle qu’une image administrative ou une image d’installation non compressée à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="8fd82-131">Creating a patch requires an uncompressed setup image, such as an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="8fd82-132">UiCreatePatchPackage ne génère pas de correctifs binaires pour les fichiers dans les armoires.</span><span class="sxs-lookup"><span data-stu-id="8fd82-132">UiCreatePatchPackage does not generate binary patches for files in cabinets.</span></span>

 

 



