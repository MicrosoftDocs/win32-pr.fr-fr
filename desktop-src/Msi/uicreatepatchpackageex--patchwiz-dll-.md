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
# <a name="uicreatepatchpackageex-patchwizdll"></a>UiCreatePatchPackageEx (Patchwiz.dll)

La fonction UiCreatePatchPackageEx prend un fichier de création de package (fichier. PCP) et génère une Windows Installer package correctif (package. msp). L’appel de [Msimsp.exe](msimsp-exe.md) est la méthode recommandée pour utiliser [Patchwiz.dll](patchwiz-dll.md).

La fonction UiCreatePatchPackageEx est disponible à partir de Patchwiz.dll version 4,0 et étend les fonctionnalités de la fonction [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

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

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

Chemin d’accès complet au fichier de propriétés de création de correctif (fichier. PCP) de ce correctif.

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

Chemin d’accès complet au package de correctifs Windows Installer (fichier. msp) à créer. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis. Si la valeur est **null** ou est une chaîne vide, la fonction utilise la valeur de PatchOutputPath dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md).

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

Emplacement des fichiers temporaires. Ce paramètre peut avoir la **valeur null** ou être une chaîne vide, mais ne peut pas être omis. L’utilisateur doit disposer des privilèges suffisants pour lire et écrire dans ce dossier. L’emplacement par défaut est% TMP% \\ ~ PCW \_ tmp. tmp \\ .

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

Si la **valeur est true**, supprimez le dossier temporaire et tout son contenu, le cas échéant. Si la **valeur est false** et que le dossier est présent, la fonction échoue.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Ce paramètre peut prendre la valeur d’une ou d’une combinaison des valeurs suivantes pour spécifier les options de journalisation ou d’interface utilisateur.



| Indicateur            | Valeur       | Signification                                  |
|-----------------|-------------|------------------------------------------|
| LOGNONE         | 0x00000000  | Écrire aucun message dans le journal.            |
| LOGINFO         | 0x00000001  | Écrire des messages d’information dans le journal. |
| LOGWARN         | 0x00000002  | Écrire les avertissements dans le journal.               |
| LOGERR          | 0x00000004  | Écrire les messages d’erreur dans le journal.         |
| LOGPERFMESSAGES | 0x00000008  | Écrire les messages de performance dans le journal.   |
| UINONE          | 0x00000000f | N’affiche pas l’interface utilisateur.       |
| UIALL           | 0x00000010  | Affichez l’interface utilisateur.              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*dwReserved*
</dt> <dd>

Réservé. Ce paramètre doit avoir la valeur zéro.

</dd> </dl>

## <a name="return-values"></a>Valeurs de retour

Consultez le tableau dans [valeurs de retour pour UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).

## <a name="remarks"></a>Notes

Pour obtenir un exemple de création d’un fichier. PCP et l’utilisation de [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) pour générer un package de correctifs Windows Installer, consultez la section [exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).

La création d’un correctif requiert une image d’installation non compressée, telle qu’une image administrative ou une image d’installation non compressée à partir d’un CD-ROM. [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) ne génère pas de correctifs binaires pour les fichiers dans les armoires.

 

 



