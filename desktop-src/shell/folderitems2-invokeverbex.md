---
description: Exécute un verbe sur une collection d’objets FolderItem. Cette méthode est une extension de la méthode InvokeVerb, qui permet un contrôle supplémentaire de l’opération via un ensemble d’indicateurs.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Méthode FolderItems2. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971879"
---
# <a name="folderitems2invokeverbex-method"></a>Méthode FolderItems2. InvokeVerbEx

Exécute un verbe sur une collection d’objets [**FolderItem**](folderitem.md) . Cette méthode est une extension de la méthode [**InvokeVerb**](folderitem-invokeverb.md) , qui permet un contrôle supplémentaire de l’opération via un ensemble d’indicateurs.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vVerb* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

**Variant** avec la chaîne de verbe qui correspond à la commande à exécuter. Si aucun verbe n’est spécifié, le verbe par défaut est exécuté.

</dd> <dt>

*vArgs* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

**Variant** qui se compose d’une chaîne avec un ou plusieurs arguments de la commande spécifiée par *vVerb*. Le format de cette chaîne dépend du verbe particulier.

</dd> </dl>

## <a name="remarks"></a>Notes

Un verbe est une chaîne utilisée pour spécifier une action particulière associée à un élément ou à une collection d’éléments. En règle générale, l’appel d’un verbe lance une application associée. Par exemple, l’appel du verbe **Open** sur un fichier. txt ouvre normalement le fichier avec un éditeur de texte, généralement Microsoft Notepad. Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **InvokeVerbEx** pour appeler le verbe par défaut (« Open ») sur **poste de travail**. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic :


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
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

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




