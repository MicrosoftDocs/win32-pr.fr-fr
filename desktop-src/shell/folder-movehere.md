---
description: Déplace un élément ou des éléments vers ce dossier.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Méthode Folder. MoveHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749180"
---
# <a name="foldermovehere-method"></a>Folder. MoveHere, méthode

Déplace un élément ou des éléments vers ce dossier.

## <a name="syntax"></a>Syntaxe


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* \[ dans\]
</dt> <dd>

Type : **variante**

Élément ou éléments à déplacer. Il peut s’agir d’une chaîne qui représente un nom de fichier, un objet [**FolderItem**](folderitem.md) ou un objet [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Options pour l’opération de déplacement. Cette valeur peut être zéro ou une combinaison des valeurs suivantes. Ces valeurs sont basées sur les indicateurs définis pour une utilisation avec le membre **fFlags** de la structure C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Ces indicateurs ne sont pas définis comme tels pour Visual Basic, VBScript ou JScript. vous devez donc les définir vous-même ou utiliser leurs équivalents numériques.

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



 (9182)


</dt> <dd>

[Version 5,0.](versions.md) Ne pas déplacer les fichiers connectés en tant que groupe. Déplacer uniquement les fichiers spécifiés.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

> [!Note]  
> Toutes les méthodes ne sont pas implémentées pour tous les dossiers. Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL). Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.

 

## <a name="examples"></a>Exemples

L’exemple suivant utilise **MoveHere** pour déplacer le fichier Temp.txt du répertoire racine du lecteur c vers le dossier c : \\ Windows. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic :


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
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



 

 




