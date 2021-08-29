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
ms.openlocfilehash: 494c6b2926b204225b4afbf41b6271209f8be0abab4432f242ef4a5bd9c26cff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884419"
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

## <a name="remarks"></a>Remarques

Un verbe est une chaîne utilisée pour spécifier une action particulière prise en charge par un élément. En règle générale, l’appel d’un verbe lance une application associée. par exemple, l’appel du verbe **open** sur un fichier .txt ouvre normalement le fichier avec un éditeur de texte, généralement Microsoft Bloc-notes. L’objet [**FolderItemVerbs**](folderitemverbs.md) représente la collection de verbes associée à l’élément. Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md).

Cette méthode est similaire à [**InvokeVerb**](folderitem-invokeverb.md), mais elle vous permet de spécifier des arguments pour la commande, ainsi que pour la commande elle-même.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation appropriée de cette méthode dans JScript, VBScript et Visual Basic.

JScript :


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




