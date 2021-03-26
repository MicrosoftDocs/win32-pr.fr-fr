---
description: Copie un ou des éléments dans un dossier.
title: Méthode Folder. CopyHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991592"
---
# <a name="foldercopyhere-method"></a>Folder. CopyHere, méthode

Copie un ou des éléments dans un dossier.

## <a name="syntax"></a>Syntaxe


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* 
</dt> <dd>

Type : **variante**

Élément ou éléments à copier. Il peut s’agir d’une chaîne qui représente un nom de fichier, un objet [**FolderItem**](folderitem.md) ou un objet [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ facultatif\]
</dt> <dd>

Type : **variante**

Options pour l’opération de copie. Cette valeur peut être zéro ou une combinaison des valeurs suivantes. Ces valeurs sont basées sur les indicateurs définis pour une utilisation avec le membre **fFlags** de la structure C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Chaque espace de noms de Shell doit fournir sa propre implémentation de ces indicateurs, et chaque espace de noms peut choisir d’ignorer certains ou même tous ces indicateurs. Ces indicateurs ne sont pas définis par nom pour Visual Basic, VBScript ou JScript. vous devez donc les définir vous-même ou utiliser leurs équivalents numériques.

> [!Note]  
> Dans certains cas, tels que les fichiers compressés (. zip), certains indicateurs d’option peuvent être ignorés par la conception.

 

<dt>



 (4)


</dt> <dd>

Ne pas afficher de boîte de dialogue de progression.

</dd> <dt>



 (8)


</dt> <dd>

Donnez au fichier utilisé un nouveau nom dans une opération de déplacement, de copie ou de changement de nom si un fichier portant le nom cible existe déjà.

</dd> <dt>



 (16)


</dt> <dd>

Répondre avec « Oui pour tout » pour une boîte de dialogue qui s’affiche.

</dd> <dt>



 (64)


</dt> <dd>

Conserver les informations d’annulation, si possible.

</dd> <dt>



 (128)


</dt> <dd>

Effectue l’opération sur les fichiers uniquement si un nom de fichier générique ( \* . \* ) est spécifié.

</dd> <dt>



 (256)


</dt> <dd>

Affiche une boîte de dialogue de progression, mais n’affiche pas les noms de fichiers.

</dd> <dt>



 (512)


</dt> <dd>

Ne confirmez pas la création d’un nouveau répertoire si l’opération requiert la création d’un répertoire.

</dd> <dt>



 (1024)


</dt> <dd>

N’affiche pas d’interface utilisateur si une erreur se produit.

</dd> <dt>



 (2048)


</dt> <dd>

[Version 4,71.](versions.md) Ne copiez pas les attributs de sécurité du fichier.

</dd> <dt>



 (4096)


</dt> <dd>

Ne fonctionne que dans le répertoire local. Ne pas utiliser de manière récursive dans les sous-répertoires.

</dd> <dt>



 (8192)


</dt> <dd>

[Version 5,0.](versions.md) Ne copiez pas les fichiers connectés en tant que groupe. Copiez uniquement les fichiers spécifiés.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Aucune notification n’est donnée au programme appelant pour indiquer que la copie est terminée.

> [!Note]  
> Toutes les méthodes ne sont pas implémentées pour tous les dossiers. Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL). Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.

 

## <a name="examples"></a>Exemples

L’exemple suivant utilise **CopyHere** pour copier le fichier Autoexec.bat du répertoire racine vers le répertoire C : \\ Windows. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



VBScript


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic :


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Dossier**](folder.md)
</dt> </dl>

 

 




