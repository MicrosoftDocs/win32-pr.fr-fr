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
ms.openlocfilehash: 85a16d3e63ef46ad2c536103a4e462a3e830e17f56f83cdcf39bbad5a33ebb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419754"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Méthode Copy de la \_ classe Directory Win32

La méthode **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copie le fichier d’entrée de répertoire logique ou le répertoire spécifié dans le chemin d’accès de l’objet vers l’emplacement spécifié par le paramètre d’entrée. Une copie n’est pas prise en charge si le remplacement d’un fichier logique existant est nécessaire.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FileName* 
</dt> <dd>

Nom complet de la copie du fichier (ou du répertoire). Exemple : c : \\ temp \\ newDirectory

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si le fichier a été copié avec succès, et tout autre nombre pour indiquer une erreur.

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

## <a name="remarks"></a>Remarques

Les dossiers doivent souvent être copiés d’un emplacement à un autre. Par exemple, vous pouvez copier un dossier d’un serveur vers un autre pour créer une copie de sauvegarde de ce dossier. Vous pouvez également avoir un dossier de modèles qui doit être copié sur les stations de travail des utilisateurs ou un dossier de scripts qui doit être copié sur tous vos serveurs DNS.

La \_ méthode de copie d’annuaire Win32 vous permet de copier un dossier d’un emplacement à un autre, sur le même ordinateur (par exemple, en copiant un dossier du lecteur C vers le lecteur D) ou sur un ordinateur distant. Pour copier un dossier, vous devez retourner une instance du dossier à copier, puis appeler la méthode Copy, en passant en tant que paramètre l’emplacement cible de la nouvelle copie du dossier. Par exemple, cette ligne de code copie un dossier dans le dossier scripts sur le lecteur F :

`objFolder.Copy("F:\Scripts")`

WMI ne remplacera pas un dossier existant lors de l’exécution de la méthode de copie. Cela signifie que l’opération de copie échoue si le dossier de destination existe. Supposons, par exemple, que vous avez un dossier nommé scripts et que vous tentez de copier ce dossier sur un partage distant nommé \\ \\ Archive ATL-FS-01 \\ . Si un dossier nommé scripts existe déjà sur ce partage, l’opération de copie échoue.

## <a name="examples"></a>Exemples

L’exemple de code proposition, extrait de la [copie d’un dossier à l’aide de WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), utilise la méthode Copy pour copier le dossier C : \\ scripts vers D : \\ archive.


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

 

