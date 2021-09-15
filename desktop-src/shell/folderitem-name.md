---
description: Définit ou obtient le nom de l’élément.
ms.assetid: 079efc8d-3d08-48b1-bdb1-83f4b89fd633
title: Propriété FolderItem.Name (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5eb757455b8bbbd4161eae477ca4677eef4fc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412525"
---
# <a name="folderitemname-property"></a>Propriété FolderItem.Name

Définit ou obtient le nom de l’élément.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
strName = FolderItem.Name
FolderItem.Name = strName
```



## <a name="property-value"></a>Valeur de la propriété

Variable de type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) qui spécifie ou reçoit le nom de l’élément.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **Name** pour récupérer le nom du fichier Autoexec.bat, puis réinitialisez le nom sur Test.bat. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnNameGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        
        objFolder2 = objShell.NameSpace("C:\\");
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Name;
                objFolderItem.Name = "TEST.BAT";
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnNameGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
                
            set objFolder2 = objShell.NameSpace("C:\")
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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
Private Sub fnNameGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\")
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
