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
# <a name="rename-method-of-the-win32_directory-class"></a>Renommer la méthode de la \_ classe Directory Win32

La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le fichier d’entrée de répertoire spécifié dans le chemin d’accès de l’objet. Un changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileName* 
</dt> <dd>

Nouveau nom complet du fichier (ou répertoire). Exemple : c : \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si le fichier a été renommé avec succès, et tout autre nombre pour indiquer une erreur.

<dl> <dt>

**0**
</dt> <dd>

La demande a abouti.

</dd> <dt>

**2**
</dt> <dd>

L’accès a été refusé.

</dd> <dt>

**8**
</dt> <dd>

Une erreur non spécifiée s’est produite.

</dd> <dt>

**9**
</dt> <dd>

Le nom spécifié n’est pas valide.

</dd> <dt>

**10**
</dt> <dd>

L’objet spécifié existe déjà.

</dd> <dt>

**11**
</dt> <dd>

Le système de fichiers n’est pas NTFS.

</dd> <dt>

**12**
</dt> <dd>

La plateforme n’est pas Windows.

</dd> <dt>

**13**
</dt> <dd>

Le lecteur n’est pas le même.

</dd> <dt>

**14**
</dt> <dd>

Le répertoire n'est pas vide.

</dd> <dt>

**15**
</dt> <dd>

Une violation de partage s’est produite.

</dd> <dt>

**16**
</dt> <dd>

Le fichier de démarrage spécifié n’est pas valide.

</dd> <dt>

**17**
</dt> <dd>

Un privilège requis pour l’opération n’est pas conservé.

</dd> <dt>

**21**
</dt> <dd>

Un paramètre spécifié n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour renommer un dossier, commencez par lier le dossier en question, puis appelez la méthode Rename. Comme seul paramètre de la méthode, transmettez le nouveau nom du dossier sous la forme d’un nom de chemin d’accès complet. Par exemple, si le dossier de la \\ sauvegarde journaux c : scripts doit \\ \\ être renommé en c : \\ scripts \\ Archive, vous devez passer l’archive c : \\ scripts \\ comme nom de dossier complet. Le passage uniquement du nom de dossier-archive-génère une erreur de chemin d’accès non valide.

La \_ classe de répertoire Win32 ne fournit pas de méthode en une étape pour déplacer des dossiers. Au lieu de cela, le déplacement d’un dossier implique généralement deux étapes :

<dl> 1. Copie du dossier vers son nouvel emplacement  
2. Suppression du dossier d’origine  
</dl>

La seule exception à ce processus en deux étapes implique le déplacement d’un dossier vers un nouvel emplacement sur le même lecteur. Supposons, par exemple, que vous souhaitiez déplacer l' \\ Archive de fichiers temporaires c : Temp vers c : \\ scripts \\ \\ . Tant que l’emplacement actuel et le nouvel emplacement se trouvent sur le même lecteur, vous pouvez déplacer le dossier en appelant simplement la méthode Rename et en passant le nouvel emplacement en tant que paramètre de méthode. Cette approche vous permet de déplacer le dossier en une seule étape. Toutefois, le script échoue si le lecteur actif et le nouveau lecteur sont différents. Une tentative de changement de nom de C : \\ temp en D : \\ temp échoue avec une erreur « lecteur non identique ».

## <a name="examples"></a>Exemples

Le code suivant, extrait de l’exemple de [déplacement d’un dossier à l’aide](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) de VBScript WMI sur la Galerie TechNet, utilise la méthode Rename pour déplacer le dossier c : \\ scripts vers c : \\ admins \\ documents \\ Archive \\ VBScript.


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Répertoire Win32**](win32-directory.md)
</dt> </dl>

 

