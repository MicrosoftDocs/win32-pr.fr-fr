---
description: Exécute un verbe sur un élément de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Méthode ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972451"
---
# <a name="shellfolderiteminvokeverbex-method"></a>Méthode ShellFolderItem. InvokeVerbEx

Exécute un verbe sur un élément de Shell.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vVerb* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

**Variant** qui contient la chaîne de verbes qui correspond à la commande à exécuter. Il doit s’agir de l’une des valeurs retournées par la propriété [**Name**](folderitemverb-name.md) de l’élément. Si aucun verbe n’est spécifié, le verbe par défaut est exécuté.

</dd> <dt>

*vArgs* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

**Variant** qui se compose d’une chaîne avec un ou plusieurs arguments de la commande spécifiée par *vVerb*. Le format de cette chaîne dépend du verbe particulier.

</dd> </dl>

## <a name="remarks"></a>Notes

Un verbe est une chaîne utilisée pour spécifier une action particulière prise en charge par un élément. En règle générale, l’appel d’un verbe lance une application associée. Par exemple, l’appel du verbe **Open** sur un fichier. txt ouvre normalement le fichier avec un éditeur de texte, généralement Microsoft Notepad. L’objet [**FolderItemVerbs**](folderitemverbs.md) représente la collection de verbes associée à l’élément. Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md).

Cette méthode est similaire à [**InvokeVerb**](folderitem-invokeverb.md), mais elle vous permet de spécifier des arguments pour la commande, ainsi que pour la commande elle-même.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation appropriée de cette méthode dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




