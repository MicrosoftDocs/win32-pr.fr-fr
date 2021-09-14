---
description: la fonction UiCreatePatchPackage prend un fichier de création de package (fichier. pcp) et génère une Windows Installer package correctif (package. msp).
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: UiCreatePatchPackage (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011823"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll)

la fonction UiCreatePatchPackage prend un fichier de création de package (fichier. pcp) et génère une Windows Installer package correctif (package. msp). L’appel de [Msimsp.exe](msimsp-exe.md) est la méthode recommandée pour utiliser [Patchwiz.dll](patchwiz-dll.md). La fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) est disponible dans la version 4,0 de Patchwiz.dll et étend les fonctionnalités de la fonction UiCreatePatchPackage.

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

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Chemin d’accès complet au fichier de propriétés de création de correctif (fichier. PCP) de ce correctif.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

chemin d’accès complet au package de correctifs Windows Installer (fichier. msp) à créer. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis. Si la valeur est **null** ou est une chaîne vide, la fonction utilise la valeur de PatchOutputPath dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

Chemin d’accès complet à un fichier journal texte qui sera ajouté. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

Handle d’une fenêtre qui affiche le texte d’État. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis.

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

Emplacement des fichiers temporaires. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis. L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Si la **valeur est true**, supprimez le dossier temporaire et tout son contenu, le cas échéant. Si la **valeur est false** et que le dossier est présent, la fonction échoue.

</dd> </dl>

## <a name="return-values"></a>Valeurs de retour

Consultez le tableau dans [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Notes

pour obtenir un exemple de création d’un fichier. pcp et l’utilisation de UiCreatePatchPackage pour générer un package de correctifs Windows Installer, consultez la section [exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).

La création d’un correctif requiert une image d’installation non compressée, telle qu’une image administrative ou une image d’installation non compressée à partir d’un CD-ROM. UiCreatePatchPackage ne génère pas de correctifs binaires pour les fichiers dans les armoires.

 

 



