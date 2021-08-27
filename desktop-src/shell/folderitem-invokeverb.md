---
description: Exécute un verbe sur l’élément.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Méthode FolderItem. InvokeVerb (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111789"
---
# <a name="folderiteminvokeverb-method"></a>Méthode FolderItem. InvokeVerb

Exécute un verbe sur l’élément.

## <a name="syntax"></a>Syntaxe


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vVerb* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Chaîne qui spécifie le verbe à exécuter. Il doit s’agir de l’une des valeurs retournées par la propriété [**FolderItemVerb.Name**](folderitemverb-name.md) de l’élément. Si aucun verbe n’est spécifié, le verbe par défaut est appelé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Un verbe est une chaîne utilisée pour spécifier une action particulière prise en charge par un élément. L’appel d’un verbe équivaut à sélectionner une commande dans le menu contextuel d’un élément. En règle générale, l’appel d’un verbe lance une application associée. par exemple, l’appel du verbe « open » sur un fichier .txt ouvre le fichier avec un éditeur de texte, généralement Microsoft Bloc-notes. Pour plus d’informations sur les verbes, consultez [lancement d’applications](launch.md) .

L’objet [**FolderItemVerbs**](folderitemverbs.md) représente la collection de verbes associée à l’élément. Le verbe par défaut peut varier pour différents éléments, mais il est généralement « Open ».

## <a name="examples"></a>Exemples

l’exemple suivant utilise **InvokeVerb** pour appeler le verbe par défaut (« open » dans ce cas) dans le dossier Windows. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verbes**](folderitem-verbs.md)
</dt> <dt>

[**DoIt**](folderitemverb-doit.md)
</dt> </dl>

 

 




